---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 7476E6DC-6DE6-4199-A680-5717053A8CC5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Remove-AzureRmServerManagementSession.md
ms.openlocfilehash: d34678b6ff7996eabf807c92a84d647af15f6a71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496864"
---
# <span data-ttu-id="4c12e-101">Remove-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="4c12e-101">Remove-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="4c12e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4c12e-102">SYNOPSIS</span></span>
<span data-ttu-id="4c12e-103">Kiszolgáló-kezelési munkamenet eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="4c12e-103">Removes a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c12e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4c12e-104">SYNTAX</span></span>

### <span data-ttu-id="4c12e-105">ByName</span><span class="sxs-lookup"><span data-stu-id="4c12e-105">ByName</span></span>
```
Remove-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4c12e-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="4c12e-106">ByObject</span></span>
```
Remove-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c12e-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4c12e-107">DESCRIPTION</span></span>
<span data-ttu-id="4c12e-108">A **Remove-AzureRmServerManagementSession** parancsmag eltávolítja az Azure Server Management-munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="4c12e-108">The **Remove-AzureRmServerManagementSession** cmdlet removes an Azure Server Management session.</span></span>

## <span data-ttu-id="4c12e-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4c12e-109">EXAMPLES</span></span>

## <span data-ttu-id="4c12e-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4c12e-110">PARAMETERS</span></span>

### <span data-ttu-id="4c12e-111">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="4c12e-111">-NodeName</span></span>
<span data-ttu-id="4c12e-112">Annak a csomópontnak a neve, amelyen a parancsmag eltávolítja a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="4c12e-112">Specifies the name of the node on which this cmdlet removes the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c12e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c12e-113">-ResourceGroupName</span></span>
<span data-ttu-id="4c12e-114">Annak az erőforráscsoport a neve, amelyhez a munkamenet tartozik.</span><span class="sxs-lookup"><span data-stu-id="4c12e-114">Specifies the name of the resource group that the session belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c12e-115">-Session</span><span class="sxs-lookup"><span data-stu-id="4c12e-115">-Session</span></span>
<span data-ttu-id="4c12e-116">A parancsmag által eltávolított munkamenetet adja meg.</span><span class="sxs-lookup"><span data-stu-id="4c12e-116">Specifies the session that this cmdlet removes.</span></span>

<span data-ttu-id="4c12e-117">Ezt a paramétert használhatja a *ResourceGroupName* , az *csomópontnév* és a *munkamenet* paraméter helyett.</span><span class="sxs-lookup"><span data-stu-id="4c12e-117">This parameter may be used instead of the *ResourceGroupName* , *NodeName* and *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c12e-118">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="4c12e-118">-SessionName</span></span>
<span data-ttu-id="4c12e-119">Annak a munkamenetnek a nevét adja meg, amely a parancsmagot eltávolítja.</span><span class="sxs-lookup"><span data-stu-id="4c12e-119">Specifies the name of the session that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByObject
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c12e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c12e-120">-DefaultProfile</span></span>
<span data-ttu-id="4c12e-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4c12e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c12e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c12e-122">CommonParameters</span></span>
<span data-ttu-id="4c12e-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4c12e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c12e-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c12e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c12e-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c12e-125">INPUTS</span></span>

### <span data-ttu-id="4c12e-126">Munkamenet</span><span class="sxs-lookup"><span data-stu-id="4c12e-126">Session</span></span>
<span data-ttu-id="4c12e-127">A "Session" paraméter elfogadja a "munkamenet" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="4c12e-127">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="4c12e-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4c12e-128">OUTPUTS</span></span>

## <span data-ttu-id="4c12e-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4c12e-129">NOTES</span></span>

## <span data-ttu-id="4c12e-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4c12e-130">RELATED LINKS</span></span>

[<span data-ttu-id="4c12e-131">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="4c12e-131">Get-AzureRmServerManagementSession</span></span>](./Get-AzureRmServerManagementSession.md)

[<span data-ttu-id="4c12e-132">Új – AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="4c12e-132">New-AzureRmServerManagementSession</span></span>](./New-AzureRmServerManagementSession.md)


