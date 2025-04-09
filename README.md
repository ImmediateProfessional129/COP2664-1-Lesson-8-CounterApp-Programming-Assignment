# COP2664-1-Lesson-8-CounterApp-Programming-Assignment
This repository is a submission link for COP2664-1: Lesson 8 CounterApp Programming Assignment

import SwiftUI

struct ContentView: View {
    @State private var count = 0

    var body: some View {
        VStack(spacing: 20) {
            Text("Count: \(count)")
                .font(.largeTitle)
                .bold()

            HStack(spacing: 20) {
                Button(action: {
                    count -= 1
                }) {
                    Text("Decrement")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.red)
                        .foregroundColor(.white)
                        .cornerRadius(10)
                }

                Button(action: {
                    count = 0
                }) {
                    Text("Reset")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.gray)
                        .foregroundColor(.white)
                        .cornerRadius(10)
                }

                Button(action: {
                    count += 1
                }) {
                    Text("Increment")
                        .padding()
                        .frame(minWidth: 100)
                        .background(Color.green)
                        .foregroundColor(.white)
                        .cornerRadius(10)
                }
            }
        }
        .padding()
    }
}
