# LA-1400
Robocode Junior-Robot


```
package SalmaTanner;
import robocode.*;


public class Ursula extends JuniorRobot{

	public void run() {
	
		setColors(purple, black, purple, black ,black );
			
		while(true) {
			
			ahead(200);
			turnGunLeft(360);
			turnGunTo(scannedAngle);
			turnRight(100);
			turnGunRight(180);
			turnRight(100);
			turnGunRight(180);
			ahead(200);
		}
	}
	
	public void manyEnemies(){

		if(others>5){
		turnTo(180);
		back(100);
		}
	}

	public void onHitRobot() {

		turnAheadLeft(100, 90);
		turnGunTo(360);
		fire(1);
	}
	
	public void hitRobotBearing() {
		
 		turnBackLeft(50, 90);
	}

	public void onScannedRobot() {
	
		turnGunTo(scannedAngle);	
		fire(2);
	}

	public void onHitByBullet() {
	
		turnRight(50);
		turnAheadRight(100, 90 - hitByBulletBearing);
		fire(3);
	}
	
	public void onHitWall() {
	
		back(200);	
	}	
}
```
