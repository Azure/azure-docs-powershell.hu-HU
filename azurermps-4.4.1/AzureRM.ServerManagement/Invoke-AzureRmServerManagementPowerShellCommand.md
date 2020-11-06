---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM.ServerManagement
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: 5acd510118f2be26ba09f3e0fefbc9b0c80aae02
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496887"
---
# <span data-ttu-id="c2656-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="c2656-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="c2656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c2656-102">SYNOPSIS</span></span>
<span data-ttu-id="c2656-103">Futtat egy Windows PowerShell-parancsfájlt egy csomóponton.</span><span class="sxs-lookup"><span data-stu-id="c2656-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c2656-104">SYNTAX</span></span>

### <span data-ttu-id="c2656-105">ByName</span><span class="sxs-lookup"><span data-stu-id="c2656-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2656-106">BySession</span><span class="sxs-lookup"><span data-stu-id="c2656-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2656-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c2656-107">DESCRIPTION</span></span>
<span data-ttu-id="c2656-108">Az **AzureRmServerManagementPowerShellCommand** parancsmag a Windows PowerShell-parancsfájlokat futtatja egy Azure Server Management Gateway által kezelt csomóponton.</span><span class="sxs-lookup"><span data-stu-id="c2656-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="c2656-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c2656-109">EXAMPLES</span></span>

## <span data-ttu-id="c2656-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c2656-110">PARAMETERS</span></span>

### <span data-ttu-id="c2656-111">-Command</span><span class="sxs-lookup"><span data-stu-id="c2656-111">-Command</span></span>
<span data-ttu-id="c2656-112">A cél csomóponton futtatandó parancsfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="c2656-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: System.Management.Automation.ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2656-113">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="c2656-113">-NodeName</span></span>
<span data-ttu-id="c2656-114">Annak a csomópontnak a nevét adja meg, amelyen a parancsfájl-blokkoló fut.</span><span class="sxs-lookup"><span data-stu-id="c2656-114">Specifies the name of the node to run the script block on.</span></span>

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

### <span data-ttu-id="c2656-115">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="c2656-115">-PowerShellSessionName</span></span>
<span data-ttu-id="c2656-116">Annak a Windows PowerShell-helynek a nevét adja meg, amely a cél csomóponton van.</span><span class="sxs-lookup"><span data-stu-id="c2656-116">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2656-117">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="c2656-117">-RawOutput</span></span>
<span data-ttu-id="c2656-118">Jelzi, hogy a parancsmag a csomópont kimenetét tartalmazó teljes objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="c2656-118">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2656-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2656-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2656-120">Annak az erőforráscsoport a neve, amelyhez a csomópont tartozik.</span><span class="sxs-lookup"><span data-stu-id="c2656-120">Specifies the name of the resource group that the node belongs to.</span></span>

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

### <span data-ttu-id="c2656-121">-Session</span><span class="sxs-lookup"><span data-stu-id="c2656-121">-Session</span></span>
<span data-ttu-id="c2656-122">Azt a **munkamenet** -objektumot adja meg, amelyet a parancsmag a cél csomóponthoz való csatlakozáshoz használ.</span><span class="sxs-lookup"><span data-stu-id="c2656-122">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="c2656-123">Ezt a paramétert a *ResourceGroupName* , a *csomópontnév* , a *munkamenet* és a *PowerShellSessionName* paraméter helyett lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="c2656-123">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

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

### <span data-ttu-id="c2656-124">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="c2656-124">-SessionName</span></span>
<span data-ttu-id="c2656-125">Annak a munkamenetnek a nevét adja meg, amely a csomópontot kezeli.</span><span class="sxs-lookup"><span data-stu-id="c2656-125">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2656-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2656-126">-DefaultProfile</span></span>
<span data-ttu-id="c2656-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c2656-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2656-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2656-128">CommonParameters</span></span>
<span data-ttu-id="c2656-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c2656-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2656-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2656-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2656-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2656-131">INPUTS</span></span>

### <span data-ttu-id="c2656-132">Munkamenet</span><span class="sxs-lookup"><span data-stu-id="c2656-132">Session</span></span>
<span data-ttu-id="c2656-133">A "Session" paraméter elfogadja a "munkamenet" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="c2656-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="c2656-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c2656-134">OUTPUTS</span></span>

### <span data-ttu-id="c2656-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="c2656-135">System.Object</span></span>

## <span data-ttu-id="c2656-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c2656-136">NOTES</span></span>

## <span data-ttu-id="c2656-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c2656-137">RELATED LINKS</span></span>

[<span data-ttu-id="c2656-138">Azure Server Management parancsmagok</span><span class="sxs-lookup"><span data-stu-id="c2656-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


