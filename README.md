# ctl
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<HTML xmlns="http://www.w3.org/1999/xhtml"
      xmlns:og="http://ogp.me/ns#"
      xmlns:fb="http://www.facebook.com/2008/fbml">
<HEAD>
	<title>Utah Indigency Calculator</title>
	<meta http-equiv="Content-type" content="text/html;charset=UTF-8"/>
	<meta name="viewport" content="width=device-width; initial-scale=1.0; maximum-scale=1.0; user-scalable=0;" />
	<meta name="apple-mobile-web-app-capable" content="no" />
	<meta name="apple-mobile-web-app-status-bar-style" content="black" />
	<meta property="og:type" content="website"/>
	<meta property="og:title" content="Utah Indigency Calculator"/>
	<meta property="og:image" content=""/>
	<meta http-equiv="X-UA-Compatible" content="IE=edge" />
	<link rel="apple-touch-icon" href="https://www.qnamarkup.org/images/QnA_300.png"/>
	<link rel="stylesheet" href="//code.jquery.com/ui/1.11.1/themes/smoothness/jquery-ui.css">
  	<script src="//code.jquery.com/jquery-1.10.2.js"></script>
  	<script src="//code.jquery.com/ui/1.11.1/jquery-ui.js"></script>
</HEAD>
<BODY BGCOLOR="#ffffff" BACKGROUND="" MARGINWIDTH="0" MARGINHEIGHT="0" onLoad="startAT('1');"><style>	

	body {

		font-family: 'Palatino Linotype', 'Book Antiqua', Palatino, serif;

	}



	#rawmarkup{

		display:none;

	}

	

	#QandA img{

		width:100%;

	}



	div.main{

		min-width:300px;

		max-width:650px;

		margin: 0 auto;

	padding:0 5px 0 5px;

		}

	div.frame{

		float:left;

		width:100%;

		margin:5px 0 5px 0;

	}

	div.full{

		float:left;

		width:100%;

	}

	.button{

		padding:8px;

		margin:8px 0 0px 0;

		width:100%;

	}

	div.question_text{

		float:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		color:#ffffff;

		min-width:30px;

		background:#5489eb;

		border-radius: 15px;

		padding:10px 15px 14px 15px;

		margin-right:45px;

	}



	div.question_text a:link, div.question_text a:hover, div.question_text a:active, div.question_text a:visited{ color:#e3fbfc; } 



	div.question_arrow{

		float:left; 

		width: 0; 

		height: 0; 

		border-left: 5px solid transparent; 

		border-right: 10px solid transparent; 

		border-top: 15px solid #5489eb;

		margin:0 20px;

	}

	div.ans_text{

		float:right;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		color:#000000;

		min-width:30px;

		background:#eeeeee;

		border-radius: 15px;

		padding:10px 15px 14px 15px;

		margin-left:45px;

	}

	div.ans_arrow{

		float:right; 

		width: 0; 

		height: 0; 

		border-left: 10px solid transparent; 

		border-right: 5px solid transparent; 

		border-top: 15px solid #eeeeee;

		margin:0 20px;

	}

	div.choices{

		float:left;

		width:100%;

		margin:15px 0 0 0;

	}

	div.standard_buttons{

		float:left;

		width:100%;

		margin-top:5px;

		border-top: 1px solid #ddd; 

		padding-top:12px;		

	}

	div.credits{

		float:left;

		dispaly:none;

		width:100%;

		background:#eee;

		margin:0px 0 15px 0;

	}

	div.credit_text{

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		padding:4px 15px 10px 15px;

	}

	li.error{

		list-style-type: none;

		background:#ffdddd;

		margin: 10px 0 0 0;

		padding: 5px;

	}



	.qpad {

		float:left;

		padding:0 15px;

	}

	

	a.sbutton {

		float:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		width:48%;

		background: #eee;

		border-radius: 8px;

		padding:10px 0px 12px 0;

		margin: 0 0 3px 0;

		border: solid 1px #888;

		text-align:center;

		color: #000000;

		text-decoration: none;

	}



	a.sbutton:hover, a.sbutton:active {

		float:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		width:48%;

		background: #ddd;

		border-radius: 8px;

		padding:10px 0px 12px 0;

		margin: 0 0 3px 0;

		border: solid 1px #888;

		text-align:center;

		color: #000000;

		text-decoration: none;

	}



	a.qabutton {

		float:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		width:100%;

		background: #eee;

		border-radius: 8px;

		padding:10px 0px 12px 0;

		margin: 0 0 8px 0;

		border: solid 1px #888;

		text-align:left;

		color: #000000;

		text-decoration: none;

	}



	a.qabutton:hover, a.qabutton:active {

		float:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		width:100%;

		background: #ddd;

		border-radius: 8px;

		padding:10px 0px 12px 0;

		margin: 0 0 8px 0;

		border: solid 1px #888;

		text-align:left;

		color: #000000;

		text-decoration: none;

	}

	



	div.xdiv {

		float:left;

		width:100%;

		margin: 0 0 8px 0;

		background: #eee;

		border: solid 1px #888;

		border-radius: 8px;

	}	



	input.xinput {

		-webkit-box-sizing: border-box; /* Safari/Chrome, other WebKit */

		-moz-box-sizing: border-box;    /* Firefox, other Gecko */ 

		box-sizing: border-box;         /* Opera/IE 8+ */

		float:left;

		width:100%;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		background: #fff;

		border-top-left-radius: 8px;

		border-top-right-radius: 8px;

		padding:10px 10px 12px 10px;

		border: solid 0px #888;

		border-bottom: solid 1px #888;

		text-align:left;

		color: #000000;

		text-decoration: none;

	}

	

	a.xbutton {

		float:left;

		width:100%;

		text-align:left;

		font-family: Verdana, Geneva, sans-serif;

		font-size: 14px;

		line-height: 20px;

		background: #eee;

		border-radius: 8px;

		padding:10px 0px 12px 0px;

		color: #000000;

		text-decoration: none;

	}

	

	a.xbutton:hover, a.xbutton:active {

		border-top-left-radius: 0px;

		border-top-right-radius: 0px;

		background: #ddd;

	}

</style>
<FORM name="FORM" id="FORM"><div id="conversation" style="margin:15px auto 0 auto;padding:0 15px;max-width:500px"><link rel="stylesheet" type="text/css" href="https://suffolklitlab.org/howto/qna/style/style.css">
<div id="icon" style="background-size: 110px 99px;background-image: url('https://suffolklitlab.org/howto/qna/images/maxheadroom.gif');"></div>
<h2 style="text-align:center;">Utah Indigency Calculator</h2>
<p><b>This is a <a href="http://www.codingthelaw.org/">class project</a>. You should not rely on it as a source of legal information. It is likely incomplete.</b></p>
<p>Answer the following questions to see if someone qualifies for appointment of counsel or fee waiver.</p>

<div id='QandA' class='QandA'><div style='padding:15px;background:#ddffdd;text-align:center;'>Loading QnA...</div></div><div id='Choices' class='choices'></div><div id="rawmarkup" style="display:none;">Title%3A+Utah+Indigency+Calculator%0D%0AAuthor%3A+Jessica+Promes%0D%0ABefore%3A%3Clink+rel%3D%22stylesheet%22+type%3D%22text%2Fcss%22+href%3D%22https%3A%2F%2Fsuffolklitlab.org%2Fhowto%2Fqna%2Fstyle%2Fstyle.css%22%3E%0D%0A%3Cdiv+id%3D%22icon%22+style%3D%22background-size%3A+110px+99px%3Bbackground-image%3A+url%28%27https%3A%2F%2Fsuffolklitlab.org%2Fhowto%2Fqna%2Fimages%2Fmaxheadroom.gif%27%29%3B%22%3E%3C%2Fdiv%3E%0D%0A%3Ch2+style%3D%22text-align%3Acenter%3B%22%3EUtah+Indigency+Calculator%3C%2Fh2%3E%0D%0A%3Cp%3E%3Cb%3EThis+is+a+%3Ca+href%3D%22http%3A%2F%2Fwww.codingthelaw.org%2F%22%3Eclass+project%3C%2Fa%3E.+You+should+not+rely+on+it+as+a+source+of+legal+information.+It+is+likely+incomplete.%3C%2Fb%3E%3C%2Fp%3E%0D%0A%3Cp%3EAnswer+the+following+questions+to+see+if+someone+qualifies+for+appointment+of+counsel+or+fee+waiver.%3C%2Fp%3E%0D%0A%0D%0AQ%281%29%3ADoes+your+client+want+to+know+about+appointment+of+counsel+for+a+criminal+case+or+fee+waivers+for+a+civil+case%3F%0D%0AA%3AAppointment+of+counsel%0D%0A%09Q%281.1%29%3AGOTO%3A2%0D%0AA%3AFee+waiver%0D%0A%09Q%281.2%29%3AGOTO%3A6%0D%0AQ%282%29%3ADoes+your+client+have+sufficient+income%2C+assets%2C+credit%2C+or+other+means+to+provide+for+payment+of+legal+counsel+and+all+other+necessary+expenses+of+representation+without+depriving+them+or+their+family+of+food%2C+shelter%2C+clothing%2C+and+other+necessities%3F%0D%0AA%3AYes%0D%0A%09Q%282.1%29%3AGOTO%3A3%0D%0AA%3ANo%0D%0A%09Q%282.2%29%3AGOTO%3A4%0D%0AQ%283%29%3AIs+your+client%27s+income+level+at+or+below+150%25+of+the+US+poverty+guidelines%3F%0D%0AA%3AYes%0D%0A%09Q%283.1%29%3AGOTO%3A4%0D%0AA%3ANo%0D%0A%09Q%283.2%29%3AGOTO%3A5%0D%0AQ%284%29%3AHas+your+client+transferred+or+otherwise+disposed+of+any+assets+since+the+commission+of+the+offense+with+the+intent+of+establishing+eligibility+for+the+appointment+of+counsel+under+the+statute%3F%0D%0AA%3AYes%0D%0A%09Q%284.1%29%3AGOTO%3A5%0D%0AA%3ANo%0D%0A%09Q%284.2%29%3AYour+client+is+considered+indigent+under+the+Utah+Statute+and+should+be+eligible+for+appointment+of+counsel.%0D%0AQ%285%29%3AYour+client+might+not+be+eligible+for+appointment+of+counsel%2C+but+the+court+has+discretion+and+takes+a+number+of+factors+into+account.+Would+you+like+to+know+what+the+court+may+consider%3F%0D%0AA%3AYes%0D%0A%09Q%285.1%29%3AGOTO%3A8%0D%0AA%3ANo%2C+thanks%21%0D%0AQ%286%29%3ARemember+your+client+must+file+a+Motion+to+Waive+Fees+and+a+Financial+Affidavit+Supporting+the+Motion.%0D%0ABut+first%2C+is+your+client%E2%80%99s+income+level+above+100%25+of+the+US+poverty+guidelines%3F%0D%0AA%3AYes%0D%0A%09Q%286.1%29%3AGOTO%3A7%0D%0AA%3ANo%0D%0A%09Q%286.2%29%3AAre+your+client%E2%80%99s+expenses+less+than+their+net+income%3F%0D%0A%09A%3AYes%0D%0A%09%09Q%286.2.1%29%3AGOTO%3A7%0D%0A%09A%3ANo%0D%0A%09%09Q%286.2.2%29%3ADoes+your+client+have+any+liquid+assets+or+credit+that+can+be+used+to+pay+the+fee+without+harming+their+financial+position%3F%0D%0A%09%09A%3AYes%0D%0A%09%09%09Q%286.2.2.1%29%3AGOTO%3A7%0D%0A%09%09A%3ANo%0D%0A%09%09%09Q%286.2.2.2%29%3ADoes+your+client+have+assets+that+can+be+liquidated+or+borrowed+against+without+harming+their+financial+position%3F%0D%0A%09%09%09A%3AYes%0D%0A%09%09%09%09Q%286.2.2.2.1%29%3AGOTO%3A7%0D%0A%09%09%09A%3ANo%0D%0A%09%09%09%09Q%286.2.2.2.2%29%3ADoes+section+30-3-3+%28temporary+alimony%29+apply+to+your+client%3F%0D%0A%09%09%09%09A%3AYes%0D%0A%09%09%09%09%09Q%286.2.2.2.2.1%29%3AGOTO%3A7%0D%0A%09%09%09%09A%3ANo%0D%0A%09%09%09%09%09Q%286.2.2.2.2.2%29%3AYour+client+might+be+eligible+for+the+fee+waiver%2C+but+the+judge+has+discretion+to+find+your+client+able+to+pay.%0D%0AQ%287%29%3AYour+client+will+likely+be+considered+reasonably+able+to+pay+for+fees.%0D%0AQ%288%29%3AGet+ready%2C+it%27s+a+bit+long%21%3Cbr%3E%0D%0A%3Cbr%3EIn+making+a+determination+of+indigency%2C+the+court+shall+consider%3A%3Cbr%3E%0D%0A%28i%29+the+probable+expense+and+burden+of+defending+the+case%3B%3Cbr%3E%0D%0A%28ii%29+the+ownership+of%2C+or+any+interest+in%2C+any+tangible+or+intangible+personal+property+or+real+property%2C+or+reasonable+expectancy+of+any+such+interest%3B%3Cbr%3E%0D%0A%28iii%29+the+amounts+of+debts+owned+by+the+defendant+or+that+might+reasonably+be+incurred+by+the+defendant+because+of+illness+or+other+needs+within+the+defendant%27s+family%3B%3Cbr%3E%0D%0A%28iv%29+number%2C+ages%2C+and+relationships+of+any+dependents%3B%3Cbr%3E%0D%0A%28v%29+the+reasonableness+of+fees+and+expenses+charged+to+the+defendant+by+the+defendant%27s+attorney+and+the+scope+of+representation+undertaken+where+the+defendant+is+represented+by+privately+retained+defense+counsel%3B+and%3Cbr%3E%0D%0A%28vi%29+other+factors+considered+relevant+by+the+court.%0D%0A%0D%0A</div><div id="ondeck" name="ondeck"><div id='Q-1' name='Q-1' style='display:none;'>Does your client want to know about appointment of counsel for a criminal case or fee waivers for a civil case?
</div><div id='Q-1.1' name='Q-1.1' style='display:none;'>GOTO:2</div><div id='Q-1.2' name='Q-1.2' style='display:none;'>GOTO:6</div><div id='Q-2' name='Q-2' style='display:none;'>Does your client have sufficient income, assets, credit, or other means to provide for payment of legal counsel and all other necessary expenses of representation without depriving them or their family of food, shelter, clothing, and other necessities?
</div><div id='Q-2.1' name='Q-2.1' style='display:none;'>GOTO:3</div><div id='Q-2.2' name='Q-2.2' style='display:none;'>GOTO:4</div><div id='Q-3' name='Q-3' style='display:none;'>Is your client's income level at or below 150% of the US poverty guidelines?
</div><div id='Q-3.1' name='Q-3.1' style='display:none;'>GOTO:4</div><div id='Q-3.2' name='Q-3.2' style='display:none;'>GOTO:5</div><div id='Q-4' name='Q-4' style='display:none;'>Has your client transferred or otherwise disposed of any assets since the commission of the offense with the intent of establishing eligibility for the appointment of counsel under the statute?
</div><div id='Q-4.1' name='Q-4.1' style='display:none;'>GOTO:5</div><div id='Q-4.2' name='Q-4.2' style='display:none;'>Your client is considered indigent under the Utah Statute and should be eligible for appointment of counsel.
</div><div id='Q-5' name='Q-5' style='display:none;'>Your client might not be eligible for appointment of counsel, but the court has discretion and takes a number of factors into account. Would you like to know what the court may consider?
</div><div id='Q-5.1' name='Q-5.1' style='display:none;'>GOTO:8</div><div id='Q-6' name='Q-6' style='display:none;'>Remember your client must file a Motion to Waive Fees and a Financial Affidavit Supporting the Motion.
But first, is your client’s income level above 100% of the US poverty guidelines?
</div><div id='Q-6.1' name='Q-6.1' style='display:none;'>GOTO:7</div><div id='Q-6.2' name='Q-6.2' style='display:none;'>Are your client’s expenses less than their net income?
</div><div id='Q-6.2.1' name='Q-6.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2' name='Q-6.2.2' style='display:none;'>Does your client have any liquid assets or credit that can be used to pay the fee without harming their financial position?
</div><div id='Q-6.2.2.1' name='Q-6.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2' name='Q-6.2.2.2' style='display:none;'>Does your client have assets that can be liquidated or borrowed against without harming their financial position?
</div><div id='Q-6.2.2.2.1' name='Q-6.2.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2.2' name='Q-6.2.2.2.2' style='display:none;'>Does section 30-3-3 (temporary alimony) apply to your client?
</div><div id='Q-6.2.2.2.2.1' name='Q-6.2.2.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2.2.2' name='Q-6.2.2.2.2.2' style='display:none;'>Your client might be eligible for the fee waiver, but the judge has discretion to find your client able to pay.
</div><div id='Q-7' name='Q-7' style='display:none;'>Your client will likely be considered reasonably able to pay for fees.
</div><div id='Q-8' name='Q-8' style='display:none;'>Get ready, it's a bit long!<br>
<br>In making a determination of indigency, the court shall consider:<br>
(i) the probable expense and burden of defending the case;<br>
(ii) the ownership of, or any interest in, any tangible or intangible personal property or real property, or reasonable expectancy of any such interest;<br>
(iii) the amounts of debts owned by the defendant or that might reasonably be incurred by the defendant because of illness or other needs within the defendant's family;<br>
(iv) number, ages, and relationships of any dependents;<br>
(v) the reasonableness of fees and expenses charged to the defendant by the defendant's attorney and the scope of representation undertaken where the defendant is represented by privately retained defense counsel; and<br>
(vi) other factors considered relevant by the court.

</div><div id='A-1.1' name='A-1.1' style='display:none;'>Appointment of counsel
</div><div id='A-href-1.1' name='A-href-1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1' name='A-target-1.1' style='display:none;'></div><div id='X-1.1' name='X-1.1' style='display:none;'>Appointment of counsel</div><div id='A-1.2' name='A-1.2' style='display:none;'>Fee waiver
</div><div id='A-href-1.2' name='A-href-1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.2' name='A-target-1.2' style='display:none;'></div><div id='X-1.2' name='X-1.2' style='display:none;'>Fee waiver</div><div id='A-2.1' name='A-2.1' style='display:none;'>Yes
</div><div id='A-href-2.1' name='A-href-2.1' style='display:none;'>javascript:void('');</div><div id='A-target-2.1' name='A-target-2.1' style='display:none;'></div><div id='X-2.1' name='X-2.1' style='display:none;'>Yes</div><div id='A-2.2' name='A-2.2' style='display:none;'>No
</div><div id='A-href-2.2' name='A-href-2.2' style='display:none;'>javascript:void('');</div><div id='A-target-2.2' name='A-target-2.2' style='display:none;'></div><div id='X-2.2' name='X-2.2' style='display:none;'>No</div><div id='A-3.1' name='A-3.1' style='display:none;'>Yes
</div><div id='A-href-3.1' name='A-href-3.1' style='display:none;'>javascript:void('');</div><div id='A-target-3.1' name='A-target-3.1' style='display:none;'></div><div id='X-3.1' name='X-3.1' style='display:none;'>Yes</div><div id='A-3.2' name='A-3.2' style='display:none;'>No
</div><div id='A-href-3.2' name='A-href-3.2' style='display:none;'>javascript:void('');</div><div id='A-target-3.2' name='A-target-3.2' style='display:none;'></div><div id='X-3.2' name='X-3.2' style='display:none;'>No</div><div id='A-4.1' name='A-4.1' style='display:none;'>Yes
</div><div id='A-href-4.1' name='A-href-4.1' style='display:none;'>javascript:void('');</div><div id='A-target-4.1' name='A-target-4.1' style='display:none;'></div><div id='X-4.1' name='X-4.1' style='display:none;'>Yes</div><div id='A-4.2' name='A-4.2' style='display:none;'>No
</div><div id='A-href-4.2' name='A-href-4.2' style='display:none;'>javascript:void('');</div><div id='A-target-4.2' name='A-target-4.2' style='display:none;'></div><div id='X-4.2' name='X-4.2' style='display:none;'>No</div><div id='A-5.1' name='A-5.1' style='display:none;'>Yes
</div><div id='A-href-5.1' name='A-href-5.1' style='display:none;'>javascript:void('');</div><div id='A-target-5.1' name='A-target-5.1' style='display:none;'></div><div id='X-5.1' name='X-5.1' style='display:none;'>Yes</div><div id='A-5.2' name='A-5.2' style='display:none;'>No, thanks!
</div><div id='A-href-5.2' name='A-href-5.2' style='display:none;'>javascript:void('');</div><div id='A-target-5.2' name='A-target-5.2' style='display:none;'></div><div id='X-5.2' name='X-5.2' style='display:none;'>No, thanks!</div><div id='A-6.1' name='A-6.1' style='display:none;'>Yes
</div><div id='A-href-6.1' name='A-href-6.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.1' name='A-target-6.1' style='display:none;'></div><div id='X-6.1' name='X-6.1' style='display:none;'>Yes</div><div id='A-6.2' name='A-6.2' style='display:none;'>No
</div><div id='A-href-6.2' name='A-href-6.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2' name='A-target-6.2' style='display:none;'></div><div id='X-6.2' name='X-6.2' style='display:none;'>No</div><div id='A-6.2.1' name='A-6.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.1' name='A-href-6.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.1' name='A-target-6.2.1' style='display:none;'></div><div id='X-6.2.1' name='X-6.2.1' style='display:none;'>Yes</div><div id='A-6.2.2' name='A-6.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2' name='A-href-6.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2' name='A-target-6.2.2' style='display:none;'></div><div id='X-6.2.2' name='X-6.2.2' style='display:none;'>No</div><div id='A-6.2.2.1' name='A-6.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.1' name='A-href-6.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.1' name='A-target-6.2.2.1' style='display:none;'></div><div id='X-6.2.2.1' name='X-6.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2' name='A-6.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2' name='A-href-6.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2' name='A-target-6.2.2.2' style='display:none;'></div><div id='X-6.2.2.2' name='X-6.2.2.2' style='display:none;'>No</div><div id='A-6.2.2.2.1' name='A-6.2.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.2.1' name='A-href-6.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.1' name='A-target-6.2.2.2.1' style='display:none;'></div><div id='X-6.2.2.2.1' name='X-6.2.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2.2' name='A-6.2.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2.2' name='A-href-6.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2' name='A-target-6.2.2.2.2' style='display:none;'></div><div id='X-6.2.2.2.2' name='X-6.2.2.2.2' style='display:none;'>No</div><div id='A-6.2.2.2.2.1' name='A-6.2.2.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.2.2.1' name='A-href-6.2.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2.1' name='A-target-6.2.2.2.2.1' style='display:none;'></div><div id='X-6.2.2.2.2.1' name='X-6.2.2.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2.2.2' name='A-6.2.2.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2.2.2' name='A-href-6.2.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2.2' name='A-target-6.2.2.2.2.2' style='display:none;'></div><div id='X-6.2.2.2.2.2' name='X-6.2.2.2.2.2' style='display:none;'>No</div>
<script>
	var QVnames = [['1','1'],['1.1','1.1'],['1.2','1.2'],['2','2'],['2.1','2.1'],['2.2','2.2'],['3','3'],['3.1','3.1'],['3.2','3.2'],['4','4'],['4.1','4.1'],['4.2','4.2'],['5','5'],['5.1','5.1'],['6','6'],['6.1','6.1'],['6.2','6.2'],['6.2.1','6.2.1'],['6.2.2','6.2.2'],['6.2.2.1','6.2.2.1'],['6.2.2.2','6.2.2.2'],['6.2.2.2.1','6.2.2.2.1'],['6.2.2.2.2','6.2.2.2.2'],['6.2.2.2.2.1','6.2.2.2.2.1'],['6.2.2.2.2.2','6.2.2.2.2.2'],['7','7'],['8','8']];
</script>
</div><textarea id="original" name="original" style="display:none;" disabled="disabled"><div id='Q-1' name='Q-1' style='display:none;'>Does your client want to know about appointment of counsel for a criminal case or fee waivers for a civil case?
</div><div id='Q-1.1' name='Q-1.1' style='display:none;'>GOTO:2</div><div id='Q-1.2' name='Q-1.2' style='display:none;'>GOTO:6</div><div id='Q-2' name='Q-2' style='display:none;'>Does your client have sufficient income, assets, credit, or other means to provide for payment of legal counsel and all other necessary expenses of representation without depriving them or their family of food, shelter, clothing, and other necessities?
</div><div id='Q-2.1' name='Q-2.1' style='display:none;'>GOTO:3</div><div id='Q-2.2' name='Q-2.2' style='display:none;'>GOTO:4</div><div id='Q-3' name='Q-3' style='display:none;'>Is your client's income level at or below 150% of the US poverty guidelines?
</div><div id='Q-3.1' name='Q-3.1' style='display:none;'>GOTO:4</div><div id='Q-3.2' name='Q-3.2' style='display:none;'>GOTO:5</div><div id='Q-4' name='Q-4' style='display:none;'>Has your client transferred or otherwise disposed of any assets since the commission of the offense with the intent of establishing eligibility for the appointment of counsel under the statute?
</div><div id='Q-4.1' name='Q-4.1' style='display:none;'>GOTO:5</div><div id='Q-4.2' name='Q-4.2' style='display:none;'>Your client is considered indigent under the Utah Statute and should be eligible for appointment of counsel.
</div><div id='Q-5' name='Q-5' style='display:none;'>Your client might not be eligible for appointment of counsel, but the court has discretion and takes a number of factors into account. Would you like to know what the court may consider?
</div><div id='Q-5.1' name='Q-5.1' style='display:none;'>GOTO:8</div><div id='Q-6' name='Q-6' style='display:none;'>Remember your client must file a Motion to Waive Fees and a Financial Affidavit Supporting the Motion.
But first, is your client’s income level above 100% of the US poverty guidelines?
</div><div id='Q-6.1' name='Q-6.1' style='display:none;'>GOTO:7</div><div id='Q-6.2' name='Q-6.2' style='display:none;'>Are your client’s expenses less than their net income?
</div><div id='Q-6.2.1' name='Q-6.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2' name='Q-6.2.2' style='display:none;'>Does your client have any liquid assets or credit that can be used to pay the fee without harming their financial position?
</div><div id='Q-6.2.2.1' name='Q-6.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2' name='Q-6.2.2.2' style='display:none;'>Does your client have assets that can be liquidated or borrowed against without harming their financial position?
</div><div id='Q-6.2.2.2.1' name='Q-6.2.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2.2' name='Q-6.2.2.2.2' style='display:none;'>Does section 30-3-3 (temporary alimony) apply to your client?
</div><div id='Q-6.2.2.2.2.1' name='Q-6.2.2.2.2.1' style='display:none;'>GOTO:7</div><div id='Q-6.2.2.2.2.2' name='Q-6.2.2.2.2.2' style='display:none;'>Your client might be eligible for the fee waiver, but the judge has discretion to find your client able to pay.
</div><div id='Q-7' name='Q-7' style='display:none;'>Your client will likely be considered reasonably able to pay for fees.
</div><div id='Q-8' name='Q-8' style='display:none;'>Get ready, it's a bit long!<br>
<br>In making a determination of indigency, the court shall consider:<br>
(i) the probable expense and burden of defending the case;<br>
(ii) the ownership of, or any interest in, any tangible or intangible personal property or real property, or reasonable expectancy of any such interest;<br>
(iii) the amounts of debts owned by the defendant or that might reasonably be incurred by the defendant because of illness or other needs within the defendant's family;<br>
(iv) number, ages, and relationships of any dependents;<br>
(v) the reasonableness of fees and expenses charged to the defendant by the defendant's attorney and the scope of representation undertaken where the defendant is represented by privately retained defense counsel; and<br>
(vi) other factors considered relevant by the court.

</div><div id='A-1.1' name='A-1.1' style='display:none;'>Appointment of counsel
</div><div id='A-href-1.1' name='A-href-1.1' style='display:none;'>javascript:void('');</div><div id='A-target-1.1' name='A-target-1.1' style='display:none;'></div><div id='X-1.1' name='X-1.1' style='display:none;'>Appointment of counsel</div><div id='A-1.2' name='A-1.2' style='display:none;'>Fee waiver
</div><div id='A-href-1.2' name='A-href-1.2' style='display:none;'>javascript:void('');</div><div id='A-target-1.2' name='A-target-1.2' style='display:none;'></div><div id='X-1.2' name='X-1.2' style='display:none;'>Fee waiver</div><div id='A-2.1' name='A-2.1' style='display:none;'>Yes
</div><div id='A-href-2.1' name='A-href-2.1' style='display:none;'>javascript:void('');</div><div id='A-target-2.1' name='A-target-2.1' style='display:none;'></div><div id='X-2.1' name='X-2.1' style='display:none;'>Yes</div><div id='A-2.2' name='A-2.2' style='display:none;'>No
</div><div id='A-href-2.2' name='A-href-2.2' style='display:none;'>javascript:void('');</div><div id='A-target-2.2' name='A-target-2.2' style='display:none;'></div><div id='X-2.2' name='X-2.2' style='display:none;'>No</div><div id='A-3.1' name='A-3.1' style='display:none;'>Yes
</div><div id='A-href-3.1' name='A-href-3.1' style='display:none;'>javascript:void('');</div><div id='A-target-3.1' name='A-target-3.1' style='display:none;'></div><div id='X-3.1' name='X-3.1' style='display:none;'>Yes</div><div id='A-3.2' name='A-3.2' style='display:none;'>No
</div><div id='A-href-3.2' name='A-href-3.2' style='display:none;'>javascript:void('');</div><div id='A-target-3.2' name='A-target-3.2' style='display:none;'></div><div id='X-3.2' name='X-3.2' style='display:none;'>No</div><div id='A-4.1' name='A-4.1' style='display:none;'>Yes
</div><div id='A-href-4.1' name='A-href-4.1' style='display:none;'>javascript:void('');</div><div id='A-target-4.1' name='A-target-4.1' style='display:none;'></div><div id='X-4.1' name='X-4.1' style='display:none;'>Yes</div><div id='A-4.2' name='A-4.2' style='display:none;'>No
</div><div id='A-href-4.2' name='A-href-4.2' style='display:none;'>javascript:void('');</div><div id='A-target-4.2' name='A-target-4.2' style='display:none;'></div><div id='X-4.2' name='X-4.2' style='display:none;'>No</div><div id='A-5.1' name='A-5.1' style='display:none;'>Yes
</div><div id='A-href-5.1' name='A-href-5.1' style='display:none;'>javascript:void('');</div><div id='A-target-5.1' name='A-target-5.1' style='display:none;'></div><div id='X-5.1' name='X-5.1' style='display:none;'>Yes</div><div id='A-5.2' name='A-5.2' style='display:none;'>No, thanks!
</div><div id='A-href-5.2' name='A-href-5.2' style='display:none;'>javascript:void('');</div><div id='A-target-5.2' name='A-target-5.2' style='display:none;'></div><div id='X-5.2' name='X-5.2' style='display:none;'>No, thanks!</div><div id='A-6.1' name='A-6.1' style='display:none;'>Yes
</div><div id='A-href-6.1' name='A-href-6.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.1' name='A-target-6.1' style='display:none;'></div><div id='X-6.1' name='X-6.1' style='display:none;'>Yes</div><div id='A-6.2' name='A-6.2' style='display:none;'>No
</div><div id='A-href-6.2' name='A-href-6.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2' name='A-target-6.2' style='display:none;'></div><div id='X-6.2' name='X-6.2' style='display:none;'>No</div><div id='A-6.2.1' name='A-6.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.1' name='A-href-6.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.1' name='A-target-6.2.1' style='display:none;'></div><div id='X-6.2.1' name='X-6.2.1' style='display:none;'>Yes</div><div id='A-6.2.2' name='A-6.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2' name='A-href-6.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2' name='A-target-6.2.2' style='display:none;'></div><div id='X-6.2.2' name='X-6.2.2' style='display:none;'>No</div><div id='A-6.2.2.1' name='A-6.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.1' name='A-href-6.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.1' name='A-target-6.2.2.1' style='display:none;'></div><div id='X-6.2.2.1' name='X-6.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2' name='A-6.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2' name='A-href-6.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2' name='A-target-6.2.2.2' style='display:none;'></div><div id='X-6.2.2.2' name='X-6.2.2.2' style='display:none;'>No</div><div id='A-6.2.2.2.1' name='A-6.2.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.2.1' name='A-href-6.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.1' name='A-target-6.2.2.2.1' style='display:none;'></div><div id='X-6.2.2.2.1' name='X-6.2.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2.2' name='A-6.2.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2.2' name='A-href-6.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2' name='A-target-6.2.2.2.2' style='display:none;'></div><div id='X-6.2.2.2.2' name='X-6.2.2.2.2' style='display:none;'>No</div><div id='A-6.2.2.2.2.1' name='A-6.2.2.2.2.1' style='display:none;'>Yes
</div><div id='A-href-6.2.2.2.2.1' name='A-href-6.2.2.2.2.1' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2.1' name='A-target-6.2.2.2.2.1' style='display:none;'></div><div id='X-6.2.2.2.2.1' name='X-6.2.2.2.2.1' style='display:none;'>Yes</div><div id='A-6.2.2.2.2.2' name='A-6.2.2.2.2.2' style='display:none;'>No
</div><div id='A-href-6.2.2.2.2.2' name='A-href-6.2.2.2.2.2' style='display:none;'>javascript:void('');</div><div id='A-target-6.2.2.2.2.2' name='A-target-6.2.2.2.2.2' style='display:none;'></div><div id='X-6.2.2.2.2.2' name='X-6.2.2.2.2.2' style='display:none;'>No</div>
<script>
	var QVnames = [['1','1'],['1.1','1.1'],['1.2','1.2'],['2','2'],['2.1','2.1'],['2.2','2.2'],['3','3'],['3.1','3.1'],['3.2','3.2'],['4','4'],['4.1','4.1'],['4.2','4.2'],['5','5'],['5.1','5.1'],['6','6'],['6.1','6.1'],['6.2','6.2'],['6.2.1','6.2.1'],['6.2.2','6.2.2'],['6.2.2.1','6.2.2.1'],['6.2.2.2','6.2.2.2'],['6.2.2.2.1','6.2.2.2.1'],['6.2.2.2.2','6.2.2.2.2'],['6.2.2.2.2.1','6.2.2.2.2.1'],['6.2.2.2.2.2','6.2.2.2.2.2'],['7','7'],['8','8']];
</script>
</textarea><textarea id="transcript" name="transcript" style="display:none;" disabled="disabled"></textarea><div style="float:left;width:100%;margin:15px 0 0px 0;border-top: solid 1px #ddd;"><div id=credits class=credits style="display:none;"><div class=credit_text><p><b> Utah Indigency Calculator</b></p><p>By  Jessica Promes</p></div></div><p align=center><a href="javascript:void('');" onClick="shoh('credits');">credits</a> | <a href="https://www.qnamarkup.org/" target=_top>code your own</a></p></div></FORM></div></div>
<script type="text/javascript">
	var QNum = 0;
	var Qhtml = "";
	var Dhtml = "";
	var label = "";
	var GOTOfired = 0;
	var path = [];
	var doc_bin = [];
	var convo_bin = [];
	var freetext = 0;
	var goingback = 0;

	$("#conversation input").on("keypress", 'form', function (e) {
    	var code = e.keyCode || e.which;
    	if (code == 13) {
        	e.preventDefault();
        	return false;
    	}
	});

	function answerQ(lb,restart) {
		currentQ = label;
		label = lb;
		Dhtml = 'D-'+label;
		Qhtml = 'Q-'+label;
		var Ahtml = 'A-'+label;
		var Jhtml = 'J-'+QNum;
		var Xhtml = 'X-'+label;
		var Xihtml = 'Xi-'+label;
		
		var input_error = 0;
		if (restart == undefined) {
			var regexp = new RegExp("\<variable\>");
			//if (document.getElementById(Xihtml)) {
			//	console.log("document.getElementById("+Xihtml+").value: "+document.getElementById(Xihtml).value);
			//} else {
			//	console.log("NO document.getElementById("+Xihtml+").value: ");
			//}
			if (document.getElementById(Ahtml).innerHTML.match(regexp)) {
				document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/(^\s*|\s*$)/,"");
				if (document.getElementById(Xihtml).value == "") {
					input_error = "Your answer appears to be empty.";
					label = currentQ;
				} else {
					document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/</g,"<");
					document.getElementById(Xihtml).value = document.getElementById(Xihtml).value.replace(/>/g,">");
				}
			} 
		}
			
		if (input_error != 0) {
			alert(input_error);
			document.getElementById(Xihtml).focus();			
		} else {
			if (restart == undefined) {
				document.getElementById('QandA').innerHTML += "<div id=\"break-at-"+QNum+"\" class='frame'><div class='full'><div class='ans_text'>"+document.getElementById(Ahtml).innerHTML+"</div></div><div class='ans_arrow'></div></div></div></div>";
				// insert answer from button
				if (document.getElementById(valueis(currentQ))) {
					document.getElementById(valueis(currentQ)).outerHTML='';
				}
				if (document.getElementById(Xihtml)) {
					document.getElementById('QandA').innerHTML = "<textarea style=\"display:none;\" id=\""+valueis(currentQ)+"\" name=\""+valueis(currentQ)+"\">"+document.getElementById(Xihtml).value+"</textarea>\n" + document.getElementById('QandA').innerHTML				
				} else {
					document.getElementById('QandA').innerHTML = "<textarea style=\"display:none;\" id=\""+valueis(currentQ)+"\" name=\""+valueis(currentQ)+"\">"+document.getElementById(Xhtml).innerHTML+"</textarea>\n" + document.getElementById('QandA').innerHTML
				}
				if (document.getElementById('QandA').innerHTML.match(regexp)) {
				 	var duplicatevars = new RegExp("id=\""+document.getElementById(Xhtml).innerHTML+"(.)*"+document.getElementById(Xhtml).innerHTML+"\"","g");
					document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(duplicatevars, "");
					document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/\<variable\>(\<\/variable\>)?/, "<input type=hidden id=\""+document.getElementById(Xhtml).innerHTML+"\" name=\""+document.getElementById(Xhtml).innerHTML+"\" value=\""+document.getElementById(Xihtml).value+"\"/>"+document.getElementById(Xihtml).value);
					//document.getElementById('transcript').value = document.getElementById('transcript').value.replace(/\<variable\>(\<\/variable\>)?/, document.getElementById(Xihtml).value+"\n");
					var thisvariable = new RegExp("<(X|x)>"+document.getElementById(Xhtml).innerHTML+"<\/(X|x)>","g");
					//document.getElementById('doc').innerHTML = document.getElementById('doc').innerHTML.replace(thisvariable, document.getElementById(document.getElementById(Xhtml).innerHTML).innerHTML);
					//document.getElementById('ondeck').innerHTML = document.getElementById('ondeck').innerHTML.replace(thisvariable, document.getElementById(valueis(currentQ)).innerHTML);
					//console.log("thisvariable: "+thisvariable);
					//console.log("Variable name: "+valueis(currentQ));
					//console.log("Variable value: "+document.getElementById(valueis(currentQ)).innerHTML);
					if(document.getElementById(Ahtml).innerHTML != "") { 
						//document.getElementById('transcript').value += "USER: "+document.getElementById(Xihtml).value+"\n"; 
						convo_bin.push("USER: "+document.getElementById(Xihtml).value+"\n");
					}
				} else {
					//document.getElementById('transcript').value += "USER: "+document.getElementById(Ahtml).innerHTML+"\n";
					convo_bin.push("USER: "+document.getElementById(Ahtml).innerHTML+"\n");
				}
				document.getElementById('Choices').innerHTML = '';
				if (goingback == 0) {
					setTimeout(function() {renderQnA(Qhtml,Jhtml,Dhtml,restart)}, 300);
				} else {
					renderQnA(Qhtml,Jhtml,Dhtml,restart);
				}
			} else {
				document.getElementById('Choices').innerHTML = '';
				path = [];
				renderQnA(Qhtml,Jhtml,Dhtml,restart);			
			}

		}
		
	}


	function renderQnA(Qht,Jht,Dht,restar) {
		Dhtml = Dht;
					
		GOTOfired = 0;
		path.push(label);

		swapGOTO(Qht,Jht);

		console.log("After swap: "+GOTOfired);

		if (GOTOfired == 0) {
			document.getElementById('QandA').innerHTML += "<div id="+Jht+" style=\"float:left;width:100%;height:1px;\"> </div>";
		}
		document.getElementById('QandA').innerHTML += "<div class='frame'><div class='full'><div class='question_text'>"+swapvar(document.getElementById(Qhtml).innerHTML)+"</div></div><div class='question_arrow'></div></div>";		

		document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/(\<br\>){2}/gi,"</div></div><div class='question_arrow'></div></div></div></div><div class='frame'><div class='full'><div class='question_text'>");
		document.getElementById('QandA').innerHTML = document.getElementById('QandA').innerHTML.replace(/(\<br\> \<br\>)/gi,"<br><br>");

		// add question 
		//document.getElementById('transcript').value += swapvar("BOT: "+ document.getElementById(Qhtml).innerHTML);
		//document.getElementById('transcript').value = document.getElementById('transcript').value.replace(/(\<br\>){2}/gi,"\nBOT: ");
		this_text = swapvar("BOT: "+ document.getElementById(Qhtml).innerHTML);
		this_text = this_text.replace(/(\<br\>){2}/gi,"\nBOT: ");
		convo_bin.push(this_text);
				
		// make push doc into array in doc() cycle through array and put into output
		// maybe remove doc div
		if (document.getElementById(Dhtml)) {
			doc_bin.push([document.getElementById(Dhtml).innerHTML,currentQ]);
			console.log("Add to Doc ("+Dhtml+"): "+document.getElementById(Dhtml).innerHTML);
			//document.getElementById('doc').innerHTML += document.getElementById(Dhtml).innerHTML;
		}
						
		tmp = getElementsByIdRegExp("div", "A-"+label+"(\\.{1}\\d){1}$");
		a_href = getElementsByIdRegExp("div", "A-href-"+label+"(\\.{1}\\d){1}$");
		a_target = getElementsByIdRegExp("div", "A-target-"+label+"(\\.{1}\\d){1}$");
		tmp_x = getElementsByIdRegExp("div", "X-"+label+"(\\.{1}\\d){1}$");
		var Xishere = 0;
		for ( var i = 0; i < tmp.length; i++ ) {
			var nextlabel = tmp[i].id.substr(2);
			var Xihtml = 'Xi-'+nextlabel;
			var regexp = "\<variable\>";
			var regexp_js = "^javascript:";
			var script_call = "";
			if (tmp[i].innerHTML.match(regexp)) {
				if (a_href[i].innerHTML.match('^(_blank:)?javascript:')) {
					script_call = a_href[i].innerHTML.replace(/^(_blank:)?javascript:/gi,"");
				} else {
					if (a_href[i].innerHTML.match('^_blank:')) {
						script_call = "window.open('"+a_href[i].innerHTML.replace(/^_blank:/,"")+"','_blank');";			
					} else {
						script_call = "location.href = '"+a_href[i].innerHTML+"';";
					}
				}
				document.getElementById('Choices').innerHTML += "<div class=\"xdiv\"><input type=\""+a_target[i].innerHTML+"\" id=\""+Xihtml+"\" name=\""+Xihtml+"\" class=\"xinput\" onkeypress=\"if (event.keyCode==13){answerQ('"+nextlabel+"');"+script_call+"}\"/><a href=\"javascript:void('');\" class=\"xbutton\" onClick=\"answerQ('"+nextlabel+"');"+script_call+"\"><span class=\"qpad\">Save above text as answer.</span></a></div>";
				Xishere = Xihtml;
				freetext = Xihtml;
			} else if (a_href[i].innerHTML.match(regexp_js) && a_href[i].innerHTML != "javascript:void('');") {
				tmp[i].innerHTML = tmp[i].innerHTML.replace(/(\<br\>){2}/gi,"<br> <br>");
				var script_call = a_href[i].innerHTML.replace(/^javascript:/gi,"");
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"qabutton\" onClick=\"answerQ('"+nextlabel+"');"+script_call+"\" "+a_target[i].innerHTML+"><span class=\"qpad\">"+tmp[i].innerHTML+"</span></a>";							
				freetext = 0;
			} else {
				tmp[i].innerHTML = tmp[i].innerHTML.replace(/(\<br\>){2}/gi,"<br> <br>");
				document.getElementById('Choices').innerHTML += "<a href=\""+a_href[i].innerHTML+"\" class=\"qabutton\" onClick=\"answerQ('"+nextlabel+"');\" "+a_target[i].innerHTML+"><span class=\"qpad\">"+tmp[i].innerHTML+"</span></a>";				
				freetext = 0;
			}
		}			

		if (restar == undefined) {
			
			document.getElementById('Choices').innerHTML += "<div class=\"standard_buttons\">";
			if (QNum > 1) { 
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"sbutton\" onClick=\"goback(QNum);\">GO BACK ONE</a>";
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"sbutton\" style=\"float:right\" onClick=\"startAT('1');\">START OVER</a>";
			} else if (QNum == 1) {
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"sbutton\" onClick=\"startAT('1');\">GO BACK ONE</a>";
				document.getElementById('Choices').innerHTML += "<a href=\"javascript:void('');\" class=\"sbutton\" style=\"float:right\" onClick=\"startAT('1');\">START OVER</a>";				
			}
			document.getElementById('Choices').innerHTML += "</div>"
		}
				
		if (QNum != 0) { 
			if (goingback == 0) {
				scroll2Q(Jht,800);           	
			} else {
				window.scrollTo(0, document.getElementById(Jht).offsetTop);     		
			}
		} else if (restar != undefined) {
			window.scrollTo(0,0);
		}
		if (Xishere != 0 && window.self == window.top) {
			console.log("Set focus for: "+Xishere);
			document.getElementById(Xishere).focus();
		}
		console.log("Q#: "+QNum);
		console.log("New Path: "+path);
		QNum++;
		goingback = 0;
					
	}

	
	function swapGOTO(QH,JH) {
		var regex = new RegExp("GOTO:(\d*)(\.\d+)*");
		if (regex.test(document.getElementById(QH).innerHTML)) {
			var Qtext = document.getElementById(QH).innerHTML.match(/(GOTO:(\d*)(.\s*\d+)*)/);
			document.getElementById('QandA').innerHTML += "<div id="+JH+" style=\"float:left;width:100%;height:1px;\"> </div>";
			// Add question
			// note I added () around the < to avoid a < followed by a ? which causes problems in php
			var Qtexttrans = document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"");
			Qtexttrans = Qtexttrans.replace(/\s*$/,"");
			if (Qtexttrans != "") {
				//document.getElementById('transcript').value += swapvar("BOT: "+Qtexttrans+"\n");
				convo_bin.push(swapvar("BOT: "+Qtexttrans+"\n"));
			}
			if (document.getElementById(QH).innerHTML.match(/^GOTO:(\d*)(.\s*\d+)*/)) {
				document.getElementById('QandA').innerHTML += document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"<"+Qtext+">");
			} else {
				document.getElementById('QandA').innerHTML += "<div class='frame'><div class='full'><div class='question_text'>"+ swapvar(document.getElementById(QH).innerHTML.replace(/(<)?GOTO:(\d*)(.\s*\d+)*>?/,"<"+Qtext+">"))+"</div></div><div class='question_arrow'></div></div>";						
			}
			// replace GOTO with text
			label = Qtext[0].replace("GOTO:","");
			Qhtml = 'Q-'+label;
			if (document.getElementById(Dhtml)) {
				doc_bin.push([document.getElementById(Dhtml).innerHTML,currentQ]);
				console.log("Add to Doc ("+Dhtml+"): "+document.getElementById(Dhtml).innerHTML);
				//document.getElementById('doc').innerHTML += document.getElementById(Dhtml).innerHTML;
			}
			Dhtml = 'D-'+label;
			GOTOfired = 1;
			console.log("In swap: "+GOTOfired);
			swapGOTO(Qhtml,JH);
		}
	}

	
	function scroll2Q(id,speed) {
		var top = document.getElementById(id).offsetTop; //Getting Y of target element
		console.log("Jump to Y for ("+id+"): "+top);
		//adapted from https://github.com/Yappli/smooth-scroll
		var moving_frequency = 5; // Affects performance !
		var hop_count = speed/moving_frequency
        var getScrollTopDocumentAtBegin = document.documentElement.scrollTop + document.body.scrollTop;
        var gap = (top - getScrollTopDocumentAtBegin) / hop_count;
		for(var i = 1; i <= hop_count; i++)
        {
        	(function()
           	{
           		var hop_top_position = gap*i;
           	    setTimeout(function(){  window.scrollTo(0, hop_top_position + getScrollTopDocumentAtBegin); }, moving_frequency*i);
           	 })();
        }
	}

	function getElementsByIdIs(selectorTag, name) {
		var items = [];
		var myPosts = document.getElementsByTagName(selectorTag);
			//omitting undefined null check for brevity
			if (myPosts[0].id == name) {
				items.push(myPosts[0]);
			}
		
		return items;
	}

	function getElementsByIdRegExp(selectorTag, expression) {
		// note you need to escape \ in the expression with \, i.e., \\ = \
		var regex = new RegExp(expression);
		var items = [];
		var myPosts = document.getElementsByTagName(selectorTag);
		for (var i = 0; i < myPosts.length; i++) {
			if (regex.test(myPosts[i].id)) {
				items.push(myPosts[i]);
			}
		}
		
		return items;
	}	

	// startAT QnA
	function startAT(id) {
		document.getElementById('ondeck').innerHTML = document.getElementById('original').value;
		document.getElementById('QandA').innerHTML = "";
		//document.getElementById('transcript').value = "";
		doc_bin = [];
		convo_bin = [];
		QNum = 0;
		answerQ(id,'1');
	}
		
	//show funtion
	function show(id) { 
   		if (document.getElementById) { // DOM3 = IE5, NS6
        	document.getElementById(id).style.display = 'block';
    	} else { 
        	if (document.layers) {  
            	document.id.display = 'block';
        	} else {
                document.all.id.style.display = 'block';
        	}
    	}
	}

	//hide funtion
	function hide(id) { 
    	if (document.getElementById) { // DOM3 = IE5, NS6
        	document.getElementById(id).style.display = 'none';         
    	} else { 
        	if (document.layers) {  
                document.id.display = 'none';
        	} else {
                document.all.id.style.display = 'none';
        	}
    	}
	}

	//show OR hide funtion depends on if element is shown or hidden
	function shoh(id) { 
    	if (document.getElementById) { // DOM3 = IE5, NS6
        	if (document.getElementById(id).style.display == "none"){
            	document.getElementById(id).style.display = 'block';
        	} else {
            	document.getElementById(id).style.display = 'none';         
        	}   
    	} else { 
        	if (document.layers) {  
            	if (document.id.display == "none"){
                	document.id.display = 'block';
            	} else {
                	document.id.display = 'none';
            	}
        	} else {
            	if (document.all.id.style.visibility == "none"){
                	document.all.id.style.display = 'block';
            	} else {
                	document.all.id.style.display = 'none';
            	}
        	}
    	}
	}
	
	function swapvar(input) {
		var output; 
		for(var i = 0; i < QVnames.length; i++) {
			if (document.getElementById(QVnames[i][1])) {
				var item = QVnames[i][1].replace(/\./g,"\\.");
				var varegx = new RegExp("<x>"+item+"<\/x>","gi");
				//console.log(QVnames[i][1]);
				input = input.replace(varegx,document.getElementById(QVnames[i][1]).innerHTML);
			} 
		}
		output = input
		return output
	}
	
	function docforindex(indexID) {
		for(var i = 0; i < doc_bin.length; i++) {
			if(doc_bin[i][1] == indexID) {
				return true;
			}
		}
	}
	function indexis(variablename) {
		for(var i = 0; i < QVnames.length; i++) {
			if(QVnames[i][1] == variablename) {
				return QVnames[i][0];
			}
		}
	}
	function valueis(variablekey) {
		for(var i = 0; i < QVnames.length; i++) {
			if(QVnames[i][0] == variablekey) {
				return QVnames[i][1];
			}
		}
	}
	
	function look4goto(qn,id) {
		console.log("GOTO SEARCH: "+id);
		var qID = "Q-"+id;
		// If there's a doc in the XXXXXXXXXXXXXXXX, remove it.
		if (docforindex(path.indexOf(id))) {
			console.log("DOC FOUND "+id);
			doc_bin.splice(doc_bin.length-1,1);
		}
		convo_bin.splice(-2,2);
		var re = new RegExp("GOTO:(([a-z0-9\._-]*)\s*)$","gi");
		if (document.getElementById(qID).innerHTML.match(re)) {
			convo_bin.splice(-1,1);
			console.log("GOTO FOUND: "+id);
			textinput = re.exec(document.getElementById(qID).innerHTML)[2]+"";
			if (docforindex(indexis(textinput))) {
				document.getElementById("Xi-"+path[qn]).value = document.getElementById(valueis(textinput)).innerHTML;
				console.log("DOC FOUND "+textinput);
				doc_bin.splice(doc_bin.length-1,1);
			}
			look4goto(qn,textinput);
		}
	}
	
	function goback(qn) {
		Qlast = qn - 3
		qn = qn - 2;
		label = path[qn];
		goingback = 1;
		
		console.log("GO BACK TO:"+qn);
		var re = new RegExp('(((^|\\n).*)*)<div id="break-at-'+qn+'" class="frame">((.*)(\\W.*))*', 'g');
		document.getElementById("QandA").innerHTML = document.getElementById("QandA").innerHTML.replace(re, '$1');
		document.getElementById('Choices').innerHTML += "<input type=\"hidden\" id=\"Xi-"+path[qn]+"\" name=\"Xi-"+path[qn]+"\" value=\"\">";
			console.log("####################: "+path[path.length-1]);
		
		//look4goto(qn,path[path.length-1]);
		
		path.splice(-1,1);
		convo_bin.splice(-4,4);
		//convo_bin.splice(-2,2);

		// If there's a doc in the last Q that you're removing, hold on to it.
		// And put it back after you've removed it. When you rerender the Q.
		if (document.getElementById("X-"+path[qn]) && document.getElementById(valueis(path[Qlast]))) {
			document.getElementById("Xi-"+path[qn]).value = document.getElementById(valueis(path[Qlast])).innerHTML;
			doc_bin.splice(doc_bin.length-1,1);
		}
		
		// If there's a doc in the current Q, remove it.
		if (docforindex(currentQ)) {
			console.log("DOC FOUND (current) "+currentQ);
			doc_bin.splice(doc_bin.length-1,1);
		}
		// If there's a doc in the queued up Q, remove it. 
		if (document.getElementById(Dhtml)) {
			console.log("DOC FOUND (ondeck)"+Dhtml);
			doc_bin.splice(doc_bin.length-1,1);
		}
		
		look4goto(qn,path[path.length-1]);
		
		if (freetext != 0) {
			document.getElementById(freetext).value = "";
		}
		QNum = qn;
		loadQ = path[path.length-1];
		path.splice(-1,1);
		
		console.log("Reload ans for: "+loadQ);
		answerQ(loadQ);
	}

	function transcript(output) {
		var convo_output = "";
		for (var i = 0, len = convo_bin.length; i < len; i++) {
			convo_output += convo_bin[i];
		}
		if (output == 1) {
			return convo_output;
		} else {
			return convo_output.replace(/<[^>]*>/g,"");
		}
	}		
	
	function doc() {
		var doc_output = ""; 
		for (var i = 0, len = doc_bin.length; i < len; i++) {
			doc_output += doc_bin[i][0];
		}
		return swapvar(doc_output);
	}	
	
	function json_str() {
		
		var json_list = "{";
		for(var i = 0; i < QVnames.length; i++) {
			if (!document.getElementById("Q-"+QVnames[i][0]).innerHTML.match(/(GOTO:(\d*)(.\s*\d+)*)/)) {
				if (document.getElementById(QVnames[i][1])) {
					json_list = json_list+'"'+QVnames[i][1]+'":"'+document.getElementById(QVnames[i][1]).innerHTML+'"';
				} else {
					json_list = json_list+'"'+QVnames[i][1]+'":"'+'"';
				}
				json_list = json_list+",";
			} 
			if (i+1 == QVnames.length) {
				json_list = json_list.replace(/,$/, '');
				json_list = json_list+"}";
			}
		}
		return json_list;
	}

	function mail2(to,subject,body) {
		to = encodeURIComponent(to);
		subject = encodeURIComponent(subject);
		body = encodeURIComponent(body);
		window.location.href = "mailto:"+to+"?subject="+subject+"&body="+body;
	}
	
	function submit2(action,method,docAs,instructions,transcriptAs,jsonAs,target) {
		document.FORM.action = action;
		document.FORM.method = method;
		if (target) {
			document.FORM.target = target;
		} else {
			document.FORM.target = "_self";		
		}
		
		if (docAs) {
			if (document.getElementsByName(docAs).length == 0) { 
				var doctext = document.createElement("textarea");
				doctext.style.display ='none';
				doctext.name= docAs;
				doctext.value= doc();
				document.getElementById('FORM').appendChild(doctext);
			} else {
				$('textarea[name='+docAs+']').val(json_str())
			}
			if (instructions) {
				if (document.getElementsByName('i').length == 0) { 
					var instructtext = document.createElement("textarea");
					instructtext.type='hidden';
					instructtext.style.display ='none';
					instructtext.name= 'i';
					instructtext.value= instructions;
					document.getElementById('FORM').appendChild(instructtext);	
				} else {
					$('textarea[name=i]').val(json_str())
				}
			}
		}
		if (transcriptAs) {
			if (document.getElementsByName(transcriptAs).length == 0) { 
				var ttext = document.createElement("textarea");
				ttext.type='hidden';
				ttext.style.display ='none';
				ttext.name= transcriptAs;
				ttext.value= transcript();
				document.getElementById('FORM').appendChild(ttext);
			} else {
				$('textarea[name='+transcriptAs+']').val(json_str())
			}
		}
		if (jsonAs) {
			if (document.getElementsByName(jsonAs).length == 0) { 
				var json = document.createElement("textarea");
				json.type='hidden';
				json.style.display ='none';
				json.name= jsonAs;			
				json.value= json_str();
				document.getElementById('FORM').appendChild(json);
			} else {
				$('textarea[name='+jsonAs+']').val(json_str())
			}
		}
		var ondeckdiv = document.getElementById('ondeck').innerHTML;
		var rawmarkupdiv = document.getElementById('rawmarkup').innerHTML;
		document.getElementById('ondeck').innerHTML = "";
		document.getElementById('rawmarkup').innerHTML = "";
		document.FORM.submit();
		document.getElementById('ondeck').innerHTML = ondeckdiv;
		document.getElementById('rawmarkup').innerHTML = rawmarkupdiv;
	}
	
	function csv() {
		var csv_list = "";
		for(var i = 0; i < QVnames.length; i++) {
			if (!document.getElementById("Q-"+QVnames[i][0]).innerHTML.match(/(GOTO:(\d*)(.\s*\d+)*)/)) {
				csv_list = csv_list+'"'+QVnames[i][1]+'"';
				csv_list = csv_list+",";
			} 
			if (i+1 == QVnames.length) {
				csv_list = csv_list.replace(/,$/, '');
				csv_list = csv_list+"\n";
			}
		}
		for(var i = 0; i < QVnames.length; i++) {
			if (!document.getElementById("Q-"+QVnames[i][0]).innerHTML.match(/(GOTO:(\d*)(.\s*\d+)*)/)) {
				if (document.getElementById(QVnames[i][1])) {
					csv_list = csv_list+'"'+document.getElementById(QVnames[i][1]).innerHTML+'"';
				} else {
					csv_list = csv_list+'""';
				}
				csv_list = csv_list+",";
			} 			
			if (i+1 == QVnames.length) {
				csv_list = csv_list.replace(/,$/, '');
				csv_list = csv_list+"\n";
			}
		}

		return csv_list;
	}
	
	function getvar(val) {
		return document.getElementById(val).value;
	}

	function goto(val) {
	   answerQ(indexis(val));
	}

	// h/t http://runnable.com/U5HC9xtufQpsu5aj/use-javascript-to-save-textarea-as-a-txt-file
	function save2(filename,content)
	{

	// I'm using file system support as a proxy for support for this feature. 
	// Check based on one found at: http://blog.teamtreehouse.com/building-an-html5-text-editor-with-the-filesystem-apis
	// Handle vendor prefixes.
	window.requestFileSystem = window.requestFileSystem || 
							   window.webkitRequestFileSystem;
	// Check for support.
	if (window.requestFileSystem) {
	// content = ID of textarea to save
	// name = name to save file as, including file extension     
	// grab the content of the form field and place it into a variable
	//    var textToWrite = document.getElementById(content).value;
	//  create a new Blob (html5 magic) that conatins the data from your form feild
		var textFileAsBlob = new Blob([content], {type:'text/plain'});
		
	// Specify the name of the file to be saved
		var fileNamecontentAs = filename;
		
	// Optionally allow the user to choose a file name by providing 
	// an imput field in the HTML and using the collected data here
	// var fileNamecontentAs = txtFileName.text;

	// create a link for our script to 'click'
		var downloadLink = document.createElement("a");
	//  supply the name of the file (from the var above).
	// you could create the name here but using a var
	// allows more flexability later.
		downloadLink.download = fileNamecontentAs;
	// provide text for the link. This will be hidden so you
	// can actually use anything you want.
		downloadLink.innerHTML = "My Hidden Link";
		
	// allow our code to work in webkit & Gecko based browsers
	// without the need for a if / else block.
		window.URL = window.URL || window.webkitURL;
			  
	// Create the link Object.
		downloadLink.href = window.URL.createObjectURL(textFileAsBlob);
	// when link is clicked call a function to remove it from
	// the DOM in case user wants to save a second file.
		downloadLink.onclick = destroyClickedElement;
	// make sure the link is hidden.
		downloadLink.style.display = "none";
	// add the link to the DOM
		document.body.appendChild(downloadLink);
		
	// click the new link
		downloadLink.click();
	} else {
		alert('This feature is not supported by your browser.');
	}
		
	}

	function destroyClickedElement(event)
	{
	// remove the link from the DOM
		document.body.removeChild(event.target);
	}

	// EOF

</script>
</BODY>
</HTML>

