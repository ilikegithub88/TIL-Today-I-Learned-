# Expo

+ 리액트 네이티브보다 편리하게 작업할 수 있고 iOS, 안드로이드 다 개발할 수 있다는 장점에 이끌려서 엑스포를 처음 이용해보았다.
+ html, 리액트에서 사용하는 `<div>` 비슷하게 엑스포에서는 `<View>`를 사용한다.
+ 글씨를 적을 때 `<Text>` 안에 적는다.
+ 아래는 엑스포에서 작성한 소스이다.

        import React from "react";
        import { StyleSheet, Text, View } from "react-native";

        export default function Loading() {
        return (
            <View style={styles.container}>
                <Text style={styles.text}> Hello </Text>
            </View>
        );
        }

        const styles = StyleSheet.create({
        container: {
            flex: 1,
            justifyContent: "flex-end",
            paddingHorizontal: 30,
            paddingVertical: 100,
            backgroundColor: "#FDF6AA"
        },
        text: {
            color: "#2c2c2c",
            fontSize: 30
        }
        });        