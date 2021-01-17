---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 9B0BBBB4-A7A0-4243-9264-362A00F5B399
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: d675c6e5b83f76451808f397427011ac3406e37a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478717"
---
# <span data-ttu-id="d5f3f-101">Get-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d5f3f-101">Get-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="d5f3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5f3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d5f3f-103">Hibrid runbook dolgozói csoportokat kap.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-103">Gets hybrid runbook worker groups.</span></span>

## <span data-ttu-id="d5f3f-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="d5f3f-104">SYNTAX</span></span>

### <span data-ttu-id="d5f3f-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d5f3f-105">ByAll (Default)</span></span>
```
Get-AzAutomationHybridWorkerGroup [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d5f3f-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d5f3f-106">ByName</span></span>
```
Get-AzAutomationHybridWorkerGroup [[-Name] <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5f3f-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="d5f3f-107">DESCRIPTION</span></span>
<span data-ttu-id="d5f3f-108">A **Get-AzAutomationHybridWorkerGroup** parancsmag megkapja az Azure Automation hibrid runbook-dolgozók csoportjait.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-108">The **Get-AzAutomationHybridWorkerGroup** cmdlet gets Azure Automation hybrid runbook worker groups.</span></span>
<span data-ttu-id="d5f3f-109">Ha egy adott csoportot is be kell szereznie, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-109">To get a specific group, specify its name.</span></span>

## <span data-ttu-id="d5f3f-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="d5f3f-110">EXAMPLES</span></span>

### <span data-ttu-id="d5f3f-111">1. példa: Az összes hibrid runbook dolgozói csoport lekérte</span><span class="sxs-lookup"><span data-stu-id="d5f3f-111">Example 1: Get all hybrid runbook worker groups</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d5f3f-112">Ez a parancs a Contoso17 nevű automatizálási fiók összes hibrid runbook-dolgozói csoportot beveszi.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-112">This command gets all hybrid runbook worker groups in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d5f3f-113">2. példa: Egyetlen hibrid runbook worker group</span><span class="sxs-lookup"><span data-stu-id="d5f3f-113">Example 2: Get a single hybrid runbook worker group</span></span>
```
PS C:\>Get-AzAutomationHybridWorkerGroup -ResourceGroupName "ResourceGroupName01" -AutomationAccountName "Contoso17" -Name "HybridRunbookWorkerGroup01"
```

<span data-ttu-id="d5f3f-114">Ez a parancs a HybridRunbookWorkerGroup01 nevű hibrid runbook worker csoportot kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-114">This command gets the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d5f3f-115">3. példa: A hibrid runbook worker group dolgozóinak be szereznie</span><span class="sxs-lookup"><span data-stu-id="d5f3f-115">Example 3: Get the workers in a hybrid runbook worker group</span></span>
```
PS C:\>(Get-AzAutomationHybridWorker -ResourceGroupName ResourceGroupName01 -AutomationAccountName Contoso17 -Name "HybridRunbookWorkerGroup01" ).RunbookWorker
```

<span data-ttu-id="d5f3f-116">Ez a parancs a HibridRunbookWorkerGroup01 nevű hibrid runbook-dolgozókat a Contoso17 nevű automatizálási fiókba veszi át.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-116">This command gets the hybrid runbook workers in the hybrid runbook worker group named HybridRunbookWorkerGroup01 in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d5f3f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5f3f-117">PARAMETERS</span></span>

### <span data-ttu-id="d5f3f-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d5f3f-118">-AutomationAccountName</span></span>
<span data-ttu-id="d5f3f-119">Egy automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-119">Specifies the name of an Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f3f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5f3f-120">-DefaultProfile</span></span>
<span data-ttu-id="d5f3f-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d5f3f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5f3f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d5f3f-122">-Name</span></span>
<span data-ttu-id="d5f3f-123">A hibrid runbook worker group nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-123">Specifies the hybrid runbook worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Group

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f3f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5f3f-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5f3f-125">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-125">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5f3f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5f3f-126">CommonParameters</span></span>
<span data-ttu-id="d5f3f-127">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5f3f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5f3f-128">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5f3f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5f3f-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d5f3f-129">INPUTS</span></span>

### <span data-ttu-id="d5f3f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d5f3f-130">System.String</span></span>

## <span data-ttu-id="d5f3f-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d5f3f-131">OUTPUTS</span></span>

### <span data-ttu-id="d5f3f-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="d5f3f-132">Microsoft.Azure.Commands.Automation.Model.HybridRunbookWorkerGroup</span></span>

## <span data-ttu-id="d5f3f-133">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="d5f3f-133">NOTES</span></span>

## <span data-ttu-id="d5f3f-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d5f3f-134">RELATED LINKS</span></span>
