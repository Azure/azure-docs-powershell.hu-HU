---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93667805"
---
# <span data-ttu-id="397b8-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="397b8-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="397b8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="397b8-102">SYNOPSIS</span></span>
<span data-ttu-id="397b8-103">Automatizálási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="397b8-103">Creates an Automation account.</span></span>

## <span data-ttu-id="397b8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="397b8-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="397b8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="397b8-105">DESCRIPTION</span></span>
<span data-ttu-id="397b8-106">A **New-AzAutomationAccount** parancsmag Azure automatizálási fiókot hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="397b8-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="397b8-107">Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.</span><span class="sxs-lookup"><span data-stu-id="397b8-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="397b8-108">Az automatizálási erőforrások közé tartozik a runbooks, a kívánt állapot-konfiguráció (DSC), a feladatok és az eszközök.</span><span class="sxs-lookup"><span data-stu-id="397b8-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="397b8-109">Példák</span><span class="sxs-lookup"><span data-stu-id="397b8-109">EXAMPLES</span></span>

### <span data-ttu-id="397b8-110">Példa 1: automatizálási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="397b8-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="397b8-111">Ez a parancs létrehoz egy ContosoAutomationAccount nevű új automatizálási fiókot a kelet-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="397b8-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="397b8-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="397b8-112">PARAMETERS</span></span>

### <span data-ttu-id="397b8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="397b8-113">-DefaultProfile</span></span>
<span data-ttu-id="397b8-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="397b8-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="397b8-115">-Hely</span><span class="sxs-lookup"><span data-stu-id="397b8-115">-Location</span></span>
<span data-ttu-id="397b8-116">Azt a helyet adja meg, ahol ez a parancsmag létrehoz egy automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="397b8-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="397b8-117">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="397b8-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397b8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="397b8-118">-Name</span></span>
<span data-ttu-id="397b8-119">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="397b8-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397b8-120">-Terv</span><span class="sxs-lookup"><span data-stu-id="397b8-120">-Plan</span></span>
<span data-ttu-id="397b8-121">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="397b8-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="397b8-122">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="397b8-122">Valid values are:</span></span>
- <span data-ttu-id="397b8-123">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="397b8-123">Basic</span></span>
- <span data-ttu-id="397b8-124">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="397b8-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397b8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="397b8-125">-ResourceGroupName</span></span>
<span data-ttu-id="397b8-126">Annak az erőforráscsoportnek a nevét adja meg, amelyre a parancsmag automatizálási fiókot ad.</span><span class="sxs-lookup"><span data-stu-id="397b8-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="397b8-127">-Címkék</span><span class="sxs-lookup"><span data-stu-id="397b8-127">-Tags</span></span>
<span data-ttu-id="397b8-128">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="397b8-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="397b8-129">Például: @ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="397b8-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="397b8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="397b8-130">CommonParameters</span></span>
<span data-ttu-id="397b8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="397b8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="397b8-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="397b8-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="397b8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="397b8-133">INPUTS</span></span>

### <span data-ttu-id="397b8-134">System. String</span><span class="sxs-lookup"><span data-stu-id="397b8-134">System.String</span></span>

### <span data-ttu-id="397b8-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="397b8-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="397b8-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="397b8-136">OUTPUTS</span></span>

### <span data-ttu-id="397b8-137">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="397b8-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="397b8-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="397b8-138">NOTES</span></span>

## <span data-ttu-id="397b8-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="397b8-139">RELATED LINKS</span></span>

[<span data-ttu-id="397b8-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="397b8-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="397b8-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="397b8-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="397b8-142">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="397b8-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
