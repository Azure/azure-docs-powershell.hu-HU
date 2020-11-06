---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 8942D757-B204-49CE-BCDE-68C3722913B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Get-AzureRmServerManagementSession.md
ms.openlocfilehash: e3388a06a2835fcd9865a9aa46d376b693152bc8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496895"
---
# <span data-ttu-id="3c923-101">Get-AzureRmServerManagementSession</span><span class="sxs-lookup"><span data-stu-id="3c923-101">Get-AzureRmServerManagementSession</span></span>

## <span data-ttu-id="3c923-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="3c923-102">SYNOPSIS</span></span>
<span data-ttu-id="3c923-103">Kiszolgáló-kezelési munkamenetet kap.</span><span class="sxs-lookup"><span data-stu-id="3c923-103">Gets a Server Management session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c923-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="3c923-104">SYNTAX</span></span>

### <span data-ttu-id="3c923-105">ByNodeName</span><span class="sxs-lookup"><span data-stu-id="3c923-105">ByNodeName</span></span>
```
Get-AzureRmServerManagementSession [-ResourceGroupName] <String> [-NodeName] <String> [-SessionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c923-106">BySession</span><span class="sxs-lookup"><span data-stu-id="3c923-106">BySession</span></span>
```
Get-AzureRmServerManagementSession [[-SessionName] <String>] [-Session] <Session>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c923-107">ByNode</span><span class="sxs-lookup"><span data-stu-id="3c923-107">ByNode</span></span>
```
Get-AzureRmServerManagementSession [-Node] <Node> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3c923-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="3c923-108">DESCRIPTION</span></span>
<span data-ttu-id="3c923-109">A **Get-AzureRmServerManagementSession** parancsmag egyetlen Azure Server Management-munkamenetet kap.</span><span class="sxs-lookup"><span data-stu-id="3c923-109">The **Get-AzureRmServerManagementSession** cmdlet gets a single Azure Server Management session.</span></span>

## <span data-ttu-id="3c923-110">Példák</span><span class="sxs-lookup"><span data-stu-id="3c923-110">EXAMPLES</span></span>

## <span data-ttu-id="3c923-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="3c923-111">PARAMETERS</span></span>

### <span data-ttu-id="3c923-112">-Node</span><span class="sxs-lookup"><span data-stu-id="3c923-112">-Node</span></span>
<span data-ttu-id="3c923-113">A *ResourceGroupName* és a *csomópontnév* paramétereinek beolvasására szolgáló meglévő **csomópont** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="3c923-113">Specifies an existing **Node** object that is used to get the *ResourceGroupName* and the *NodeName* parameters.</span></span>
<span data-ttu-id="3c923-114">A *munkamenet* paraméter értékét is meg kell adnia.</span><span class="sxs-lookup"><span data-stu-id="3c923-114">You must also specify a value for the *SessionName* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Node
Parameter Sets: ByNode
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c923-115">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="3c923-115">-NodeName</span></span>
<span data-ttu-id="3c923-116">Annak a csomópontnak a nevét adja meg, amelyben a munkamenet található.</span><span class="sxs-lookup"><span data-stu-id="3c923-116">Specifies the name of the node where the session is located.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c923-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c923-117">-ResourceGroupName</span></span>
<span data-ttu-id="3c923-118">Annak az erőforráscsoport a neve, amelyhez a parancsmag beolvassa a munkamenetet.</span><span class="sxs-lookup"><span data-stu-id="3c923-118">Specifies the name of the resource group for which this cmdlet gets the retrieve the session.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c923-119">-Session</span><span class="sxs-lookup"><span data-stu-id="3c923-119">-Session</span></span>
<span data-ttu-id="3c923-120">Azt a meglévő **munkamenet** -objektumot adja meg, amely a *ResourceGroupName* , a *csomópontnév* és a *munkamenetek* paramétereinek beolvasására szolgál.</span><span class="sxs-lookup"><span data-stu-id="3c923-120">Specifies an existing **Session** object that is used to get the *ResourceGroupName* , the *NodeName* , and the *SessionName* parameters.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServerManagement.Model.Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c923-121">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="3c923-121">-SessionName</span></span>
<span data-ttu-id="3c923-122">Annak a munkamenetnek a nevét adja meg, amelyben a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="3c923-122">Specifies the name of the session in which this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySession
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c923-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c923-123">-DefaultProfile</span></span>
<span data-ttu-id="3c923-124">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3c923-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3c923-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c923-125">CommonParameters</span></span>
<span data-ttu-id="3c923-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="3c923-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c923-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c923-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c923-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c923-128">INPUTS</span></span>

### <span data-ttu-id="3c923-129">Csomópont</span><span class="sxs-lookup"><span data-stu-id="3c923-129">Node</span></span>
<span data-ttu-id="3c923-130">A "Node" paraméter elfogadja a "csomópont" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3c923-130">Parameter 'Node' accepts value of type 'Node' from the pipeline</span></span>

### <span data-ttu-id="3c923-131">Munkamenet</span><span class="sxs-lookup"><span data-stu-id="3c923-131">Session</span></span>
<span data-ttu-id="3c923-132">A "Session" paraméter elfogadja a "munkamenet" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="3c923-132">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="3c923-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3c923-133">OUTPUTS</span></span>

### <span data-ttu-id="3c923-134">Microsoft. Azure. Command. ServerManagement. Model. Session</span><span class="sxs-lookup"><span data-stu-id="3c923-134">Microsoft.Azure.Commands.ServerManagement.Model.Session</span></span>

## <span data-ttu-id="3c923-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="3c923-135">NOTES</span></span>

## <span data-ttu-id="3c923-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3c923-136">RELATED LINKS</span></span>

[<span data-ttu-id="3c923-137">Azure Server Management parancsmagok</span><span class="sxs-lookup"><span data-stu-id="3c923-137">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


