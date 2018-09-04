# ctl
Utah Indigency Calculator
Title: Utah Indigency Calculator
Author: Jessica Promes
Before:<link rel="stylesheet" type="text/css" href="https://suffolklitlab.org/howto/qna/style/style.css">
<div id="icon" style="background-size: 110px 99px;background-image: url('https://suffolklitlab.org/howto/qna/images/maxheadroom.gif');"></div>
<h2 style="text-align:center;">Utah Indigency Calculator</h2>
<p><b>This is a <a href="http://www.codingthelaw.org/">class project</a>. You should not rely on it as a source of legal information. It is likely incomplete.</b></p>
<p>Answer the following questions to see if someone qualifies for appointment of counsel or fee waiver.</p>

Q(1):Does your client want to know about appointment of counsel for a criminal case or fee waivers for a civil case?
A:Appointment of counsel
	Q(1.1):GOTO:2
A:Fee waiver
	Q(1.2):GOTO:6
Q(2):Does your client have sufficient income, assets, credit, or other means to provide for payment of legal counsel and all other necessary expenses of representation without depriving them or their family of food, shelter, clothing, and other necessities?
A:Yes
	Q(2.1):GOTO:3
A:No
	Q(2.2):GOTO:4
Q(3):Is your client's income level at or below 150% of the US poverty guidelines?
A:Yes
	Q(3.1):GOTO:4
A:No
	Q(3.2):GOTO:5
Q(4):Has your client transferred or otherwise disposed of any assets since the commission of the offense with the intent of establishing eligibility for the appointment of counsel under the statute?
A:Yes
	Q(4.1):GOTO:5
A:No
	Q(4.2):Your client is considered indigent under the Utah Statute and should be eligible for appointment of counsel.
Q(5):Your client might not be eligible for appointment of counsel, but the court has discretion and takes a number of factors into account. Would you like to know what the court may consider?
A:Yes
	Q(5.1):GOTO:8
A:No, thanks!
Q(6):Remember your client must file a Motion to Waive Fees and a Financial Affidavit Supporting the Motion.
But first, is your client’s income level above 100% of the US poverty guidelines?
A:Yes
	Q(6.1):GOTO:7
A:No
	Q(6.2):Are your client’s expenses less than their net income?
	A:Yes
		Q(6.2.1):GOTO:7
	A:No
		Q(6.2.2):Does your client have any liquid assets or credit that can be used to pay the fee without harming their financial position?
		A:Yes
			Q(6.2.2.1):GOTO:7
		A:No
			Q(6.2.2.2):Does your client have assets that can be liquidated or borrowed against without harming their financial position?
			A:Yes
				Q(6.2.2.2.1):GOTO:7
			A:No
				Q(6.2.2.2.2):Does section 30-3-3 (temporary alimony) apply to your client?
				A:Yes
					Q(6.2.2.2.2.1):GOTO:7
				A:No
					Q(6.2.2.2.2.2):Your client might be eligible for the fee waiver, but the judge has discretion to find your client able to pay.
Q(7):Your client will likely be considered reasonably able to pay for fees.
Q(8):Get ready, it's a bit long!<br>
<br>In making a determination of indigency, the court shall consider:<br>
(i) the probable expense and burden of defending the case;<br>
(ii) the ownership of, or any interest in, any tangible or intangible personal property or real property, or reasonable expectancy of any such interest;<br>
(iii) the amounts of debts owned by the defendant or that might reasonably be incurred by the defendant because of illness or other needs within the defendant's family;<br>
(iv) number, ages, and relationships of any dependents;<br>
(v) the reasonableness of fees and expenses charged to the defendant by the defendant's attorney and the scope of representation undertaken where the defendant is represented by privately retained defense counsel; and<br>
(vi) other factors considered relevant by the court.

