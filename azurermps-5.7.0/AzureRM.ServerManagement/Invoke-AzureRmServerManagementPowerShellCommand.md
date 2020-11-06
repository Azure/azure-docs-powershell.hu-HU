---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: 1EA5F348-5EF4-4056-BA06-7B95E12E329D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/invoke-azurermservermanagementpowershellcommand
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Invoke-AzureRmServerManagementPowerShellCommand.md
ms.openlocfilehash: d4720a1159d55064a007a97df7233853200f1295
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494353"
---
# <span data-ttu-id="8e571-101">Invoke-AzureRmServerManagementPowerShellCommand</span><span class="sxs-lookup"><span data-stu-id="8e571-101">Invoke-AzureRmServerManagementPowerShellCommand</span></span>

## <span data-ttu-id="8e571-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8e571-102">SYNOPSIS</span></span>
<span data-ttu-id="8e571-103">Futtat egy Windows PowerShell-parancsfájlt egy csomóponton.</span><span class="sxs-lookup"><span data-stu-id="8e571-103">Executes a Windows PowerShell script block on a node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e571-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8e571-104">SYNTAX</span></span>

### <span data-ttu-id="8e571-105">ByName</span><span class="sxs-lookup"><span data-stu-id="8e571-105">ByName</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-ResourceGroupName] <String> [-NodeName] <String>
 [-SessionName] <String> [-Command] <ScriptBlock> [-PowerShellSessionName <String>] [-RawOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e571-106">BySession</span><span class="sxs-lookup"><span data-stu-id="8e571-106">BySession</span></span>
```
Invoke-AzureRmServerManagementPowerShellCommand [-Session] <Session> [-Command] <ScriptBlock>
 [-PowerShellSessionName <String>] [-RawOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e571-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8e571-107">DESCRIPTION</span></span>
<span data-ttu-id="8e571-108">Az **AzureRmServerManagementPowerShellCommand** parancsmag a Windows PowerShell-parancsfájlokat futtatja egy Azure Server Management Gateway által kezelt csomóponton.</span><span class="sxs-lookup"><span data-stu-id="8e571-108">The **Invoke-AzureRmServerManagementPowerShellCommand** cmdlet executes a Windows PowerShell script block on a node managed by an Azure Server Management Gateway.</span></span>

## <span data-ttu-id="8e571-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8e571-109">EXAMPLES</span></span>

## <span data-ttu-id="8e571-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8e571-110">PARAMETERS</span></span>

### <span data-ttu-id="8e571-111">-Command</span><span class="sxs-lookup"><span data-stu-id="8e571-111">-Command</span></span>
<span data-ttu-id="8e571-112">A cél csomóponton futtatandó parancsfájlt adja meg.</span><span class="sxs-lookup"><span data-stu-id="8e571-112">Specifies the script block to run on the target node.</span></span>

```yaml
Type: ScriptBlock
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e571-113">-DefaultProfile</span></span>
<span data-ttu-id="8e571-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8e571-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-115">-Csomópontnév</span><span class="sxs-lookup"><span data-stu-id="8e571-115">-NodeName</span></span>
<span data-ttu-id="8e571-116">Annak a csomópontnak a nevét adja meg, amelyen a parancsfájl-blokkoló fut.</span><span class="sxs-lookup"><span data-stu-id="8e571-116">Specifies the name of the node to run the script block on.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-117">-PowerShellSessionName</span><span class="sxs-lookup"><span data-stu-id="8e571-117">-PowerShellSessionName</span></span>
<span data-ttu-id="8e571-118">Annak a Windows PowerShell-helynek a nevét adja meg, amely a cél csomóponton van.</span><span class="sxs-lookup"><span data-stu-id="8e571-118">Specifies the name of the Windows PowerShell run space on the target node.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-119">-RawOutput</span><span class="sxs-lookup"><span data-stu-id="8e571-119">-RawOutput</span></span>
<span data-ttu-id="8e571-120">Jelzi, hogy a parancsmag a csomópont kimenetét tartalmazó teljes objektumot adja eredményül.</span><span class="sxs-lookup"><span data-stu-id="8e571-120">Indicates that the cmdlet returns the complete object that contains the output from the node.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e571-121">-ResourceGroupName</span></span>
<span data-ttu-id="8e571-122">Annak az erőforráscsoport a neve, amelyhez a csomópont tartozik.</span><span class="sxs-lookup"><span data-stu-id="8e571-122">Specifies the name of the resource group that the node belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-123">-Session</span><span class="sxs-lookup"><span data-stu-id="8e571-123">-Session</span></span>
<span data-ttu-id="8e571-124">Azt a **munkamenet** -objektumot adja meg, amelyet a parancsmag a cél csomóponthoz való csatlakozáshoz használ.</span><span class="sxs-lookup"><span data-stu-id="8e571-124">Specifies the **Session** object that this cmdlet uses to connect to the target node.</span></span>

<span data-ttu-id="8e571-125">Ezt a paramétert a *ResourceGroupName* , a *csomópontnév* , a *munkamenet* és a *PowerShellSessionName* paraméter helyett lehet megadni.</span><span class="sxs-lookup"><span data-stu-id="8e571-125">This parameter may be specified instead of the *ResourceGroupName* , *NodeName* , *SessionName* , and *PowerShellSessionName* parameters.</span></span>

```yaml
Type: Session
Parameter Sets: BySession
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-126">-Munkamenet</span><span class="sxs-lookup"><span data-stu-id="8e571-126">-SessionName</span></span>
<span data-ttu-id="8e571-127">Annak a munkamenetnek a nevét adja meg, amely a csomópontot kezeli.</span><span class="sxs-lookup"><span data-stu-id="8e571-127">Specifies the name of the session to manage the node.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e571-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e571-128">CommonParameters</span></span>
<span data-ttu-id="8e571-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8e571-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e571-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e571-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e571-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e571-131">INPUTS</span></span>

### <span data-ttu-id="8e571-132">Munkamenet</span><span class="sxs-lookup"><span data-stu-id="8e571-132">Session</span></span>
<span data-ttu-id="8e571-133">A "Session" paraméter elfogadja a "munkamenet" típusú értéket a csővezetékről</span><span class="sxs-lookup"><span data-stu-id="8e571-133">Parameter 'Session' accepts value of type 'Session' from the pipeline</span></span>

## <span data-ttu-id="8e571-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8e571-134">OUTPUTS</span></span>

### <span data-ttu-id="8e571-135">System. Object (rendszer. objektum)</span><span class="sxs-lookup"><span data-stu-id="8e571-135">System.Object</span></span>

## <span data-ttu-id="8e571-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8e571-136">NOTES</span></span>

## <span data-ttu-id="8e571-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8e571-137">RELATED LINKS</span></span>

[<span data-ttu-id="8e571-138">Azure Server Management parancsmagok</span><span class="sxs-lookup"><span data-stu-id="8e571-138">Azure Server Management Cmdlets</span></span>](./AzureRM.ServerManagement.md)


