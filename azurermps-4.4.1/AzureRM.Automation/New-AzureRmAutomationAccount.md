---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672884"
---
# <span data-ttu-id="d911a-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d911a-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="d911a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d911a-102">SYNOPSIS</span></span>
<span data-ttu-id="d911a-103">Automatizálási fiókot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d911a-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d911a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d911a-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d911a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="d911a-105">DESCRIPTION</span></span>
<span data-ttu-id="d911a-106">A **New-AzureRmAutomationAccount** parancsmag Azure automatizálási fiókot hoz létre egy erőforráscsoportben.</span><span class="sxs-lookup"><span data-stu-id="d911a-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="d911a-107">Az automatizálási fiók a többi automatizálási fiók erőforrásaitól elkülönített automatizálási erőforrások tárolója.</span><span class="sxs-lookup"><span data-stu-id="d911a-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="d911a-108">Az automatizálási erőforrások közé tartozik a runbooks, a kívánt állapot-konfiguráció (DSC), a feladatok és az eszközök.</span><span class="sxs-lookup"><span data-stu-id="d911a-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="d911a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d911a-109">EXAMPLES</span></span>

### <span data-ttu-id="d911a-110">Példa 1: automatizálási fiók létrehozása</span><span class="sxs-lookup"><span data-stu-id="d911a-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="d911a-111">Ez a parancs létrehoz egy ContosoAutomationAccount nevű új automatizálási fiókot a kelet-amerikai régióban.</span><span class="sxs-lookup"><span data-stu-id="d911a-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="d911a-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d911a-112">PARAMETERS</span></span>

### <span data-ttu-id="d911a-113">-Hely</span><span class="sxs-lookup"><span data-stu-id="d911a-113">-Location</span></span>
<span data-ttu-id="d911a-114">Azt a helyet adja meg, ahol ez a parancsmag létrehoz egy automatizálási fiókot.</span><span class="sxs-lookup"><span data-stu-id="d911a-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="d911a-115">Ha érvényes helyeket szeretne beolvasni, használja az Get-AzureRMLocation parancsmagot.</span><span class="sxs-lookup"><span data-stu-id="d911a-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="d911a-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d911a-116">-Name</span></span>
<span data-ttu-id="d911a-117">Az automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d911a-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="d911a-118">-Terv</span><span class="sxs-lookup"><span data-stu-id="d911a-118">-Plan</span></span>
<span data-ttu-id="d911a-119">Az automatizálási fiók tervét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d911a-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="d911a-120">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="d911a-120">Valid values are:</span></span>

- <span data-ttu-id="d911a-121">Egyszerű</span><span class="sxs-lookup"><span data-stu-id="d911a-121">Basic</span></span>
- <span data-ttu-id="d911a-122">Ingyenes</span><span class="sxs-lookup"><span data-stu-id="d911a-122">Free</span></span>

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

### <span data-ttu-id="d911a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d911a-123">-ResourceGroupName</span></span>
<span data-ttu-id="d911a-124">Annak az erőforráscsoportnek a nevét adja meg, amelyre a parancsmag automatizálási fiókot ad.</span><span class="sxs-lookup"><span data-stu-id="d911a-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="d911a-125">-Címkék</span><span class="sxs-lookup"><span data-stu-id="d911a-125">-Tags</span></span>
<span data-ttu-id="d911a-126">A kulcs-érték párok a hash-táblázatok formájában.</span><span class="sxs-lookup"><span data-stu-id="d911a-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d911a-127">Példa:</span><span class="sxs-lookup"><span data-stu-id="d911a-127">For example:</span></span>

<span data-ttu-id="d911a-128">@ {key0 = "value0"; key1 = $null; azonosító2 = "érték2"}</span><span class="sxs-lookup"><span data-stu-id="d911a-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d911a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d911a-129">-DefaultProfile</span></span>
<span data-ttu-id="d911a-130">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d911a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d911a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d911a-131">CommonParameters</span></span>
<span data-ttu-id="d911a-132">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d911a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d911a-133">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d911a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d911a-134">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d911a-134">INPUTS</span></span>

## <span data-ttu-id="d911a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d911a-135">OUTPUTS</span></span>

### <span data-ttu-id="d911a-136">Microsoft. Azure. Command. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d911a-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="d911a-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d911a-137">NOTES</span></span>

## <span data-ttu-id="d911a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d911a-138">RELATED LINKS</span></span>

[<span data-ttu-id="d911a-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d911a-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="d911a-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d911a-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="d911a-141">Set-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="d911a-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
