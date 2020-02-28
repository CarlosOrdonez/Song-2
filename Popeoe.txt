use_bpm 175
a ="C:/Users/carlos_ordonez/Downloads/challenge_d/travis_sounds/skrt.wav"
b ="C:/Users/carlos_ordonez/Downloads/challenge_d/travis_sounds/ohh.wav"
c ="C:/Users/carlos_ordonez/Downloads/challenge_d/travis_sounds/dope.wav"

sample "C:/Users/carlos_ordonez/Downloads/challenge_d/travis_sounds/NoCap.wav", amp: 3
#sample duration = 8.781944444444443
sleep 8.781944444444443
live_loop :randomness do
  8.times do
    sample choose([a, b, c])
    sleep 8
  end
  stop
end
live_loop :drums do
  15.times do
    sample :drum_heavy_kick
    sleep 1.5
    sample :drum_heavy_kick
    sleep 1.5
    sample :drum_heavy_kick
    sleep 0.5
    sample :drum_heavy_kick
    sleep 0.5
  end
  stop
end
live_loop :flip do
  15.times do
    sample :perc_snap, amp: 1.5
    sleep 2
    sample :perc_snap, amp: 1.5
    sleep 2
  end
  stop
end
define :poory do |n1, n2, n3, n4, n5, n6, n7, n8, x |
  play n1, amp: x
  sleep 2
  play n2, amp: x
  sleep 2
  play n3, amp: x
  sleep 2
  play n4, amp: x
  sleep 2
  play n5, amp: x
  sleep 2
  play n6, amp: x
  sleep 2
  play n7, amp: x
  sleep 2
  play n8, amp: x
  sleep 2
end


another_variable = 2

poory :c3, :e3, :g3, :b3, :c3, :b3, :g3, :e3, another_variable

use_bpm 175
define :m2 do
  print "m2 start"
  play:e4
  sleep 0.5
  play:d4
  sleep 0.5
  play:c4
  sleep 1
  play:c4
  sleep 0.5
  play:d4
  sleep 0.5
  play:c4
  sleep 0.5
  play:g3
  sleep 0.5
  play:e3
  sleep 0.5
  play:f3
  sleep 0.5
  play:g3
  sleep 0.5
  play:a3
  sleep 0.5
  play:g3
  sleep 0.5
  play:f3
  sleep 0.5
  play:g3
  sleep 1
end
live_loop:jdj do
  2.times do
    i = 0
    my_note = [:c4,:d4,:e4,:e4,:e4,:c4,:d4,:d4,:e4,:d4,:c4,:d4]
    my_sleep = [0.5, 0.5, 1, 1, 1, 0.5, 0.5, 0.5,0.5,0.5,0.5,1]
    
    my_notes = [:c4,:d4,:e4,:g4,:a4,:g4,:e4,:c4,:e4,:f4,:e4,:c4]
    my_sleeps = [0.5, 0.5, 0.5, 1, 0.5, 0.5, 0.5,0.5, 0.5,1,1,1]
    m2
    print "hey"
    i = 0
    12.times do
      play my_note[i]
      sleep my_sleep[i]
      i = i + 1
      print "turkey"
    end
    m2
    i = 0
    12.times do
      play my_notes[i]
      sleep my_sleeps[i]
      i = i + 1
      if i==0
      else print "bowwow"
      end
    end
  end
  stop
end


sleep 62
b = 4
4.times do
  b = b-1
  print "decrease the rate by 1"
  sample "C:/Users/carlos_ordonez/Downloads/challenge_d/travis_sounds/NoCap.wav", amp: b
  sleep 8.781944444444443
end




