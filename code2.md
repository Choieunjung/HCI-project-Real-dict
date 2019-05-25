## 구현코드

using System.Collections;
using System.Collections.Generic;
using UnityEngine;
using UnityEngine.SceneManagement;

public class newgame : MonoBehaviour
{
    public GameObject activity;
    private System.Diagnostics.Stopwatch stopWatch = new System.Diagnostics.Stopwatch();

    public bool selected = false;

    private void Start()
    {
        var actTransform = activity.GetComponent<RectTransform>().position;
        actTransform = GetComponent<RectTransform>().position;
       
        activity.SetActive(false);
    }

    private void Update()
    {	////해당 버튼위에 손이 있는지 확인하는 구문
        if (selected == true)
        {    ///선택됐다면 화면가운데 원형 로딩표시가 나옴
            activity.SetActive(true);

            ////2초 이상 버튼위에 손을 올리면 다른 화면으로 바뀌는 구문
            if (stopWatch.ElapsedMilliseconds > 2000.0f)
            {
                Debug.Log("바뀐다");
		///scene이 바뀌는 구문 
                SceneManager.LoadScene("CATEGORY");
            }
        }
        else
        {   ///만약 선택을 중단하면 로딩표시하는 원이 사라지고 2초이상 올리는지 확인하는게
///0초로 초기화됨
            activity.SetActive(false);
            stopWatch.Reset();
        }
    }

    private void OnTriggerEnter(Collider other)
    {   ///해당 버튼에 손가락이 닿았는지 확인하고 닿았으면 로딩중 화면과 시간이 카운터됨

        Debug.Log("들어왔다");
        selected = true;

        stopWatch.Start();
        activity.SetActive(true);
        //StartCoroutine(Wait3Sec());

    }

    private void OnTriggerExit(Collider other)
    {   ///해당 버튼에서 손가락이 나가면 로딩중 표시가 없어지고 시간초가 초기화됨
        Debug.Log("나갔다");
        selected = false;
        activity.SetActive(false);
     }
}
