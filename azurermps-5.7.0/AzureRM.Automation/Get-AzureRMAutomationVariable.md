---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationVariable.md
ms.openlocfilehash: 5fccd3f6aa193a3c2cacf39e6b72bccdf440b393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505847"
---
# <span data-ttu-id="4afe3-101">Get-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4afe3-101">Get-AzureRmAutomationVariable</span></span>

## <span data-ttu-id="4afe3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4afe3-102">SYNOPSIS</span></span>
<span data-ttu-id="4afe3-103">Automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="4afe3-103">Gets an Automation variable.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4afe3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4afe3-104">SYNTAX</span></span>

### <span data-ttu-id="4afe3-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4afe3-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4afe3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4afe3-106">ByName</span></span>
```
Get-AzureRmAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4afe3-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4afe3-107">DESCRIPTION</span></span>
<span data-ttu-id="4afe3-108">A **Get-AzureRmAutomationVariable** parancsmag egy vagy több Azure automatizálási változót kap.</span><span class="sxs-lookup"><span data-stu-id="4afe3-108">The **Get-AzureRmAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="4afe3-109">Ha meghatározott változót szeretne beszerezni, adja meg a nevét.</span><span class="sxs-lookup"><span data-stu-id="4afe3-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="4afe3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4afe3-110">EXAMPLES</span></span>

### <span data-ttu-id="4afe3-111">Példa 1: változó beszerzése</span><span class="sxs-lookup"><span data-stu-id="4afe3-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzureRmAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="4afe3-112">Az első parancs a Variable06 nevű automatizálási változót kapja a Contoso17 nevű fiókban.</span><span class="sxs-lookup"><span data-stu-id="4afe3-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="4afe3-113">A parancs az objektumot a $Variable változóban tárolja.</span><span class="sxs-lookup"><span data-stu-id="4afe3-113">The command stores that object in the $Variable variable.</span></span>

<span data-ttu-id="4afe3-114">A második parancs normál képpont jelöléssel hivatkozik $Variable **Value** tulajdonságára.</span><span class="sxs-lookup"><span data-stu-id="4afe3-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="4afe3-115">A parancs a $value változó értékét tárolja.</span><span class="sxs-lookup"><span data-stu-id="4afe3-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="4afe3-116">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4afe3-116">PARAMETERS</span></span>

### <span data-ttu-id="4afe3-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4afe3-117">-AutomationAccountName</span></span>
<span data-ttu-id="4afe3-118">Annak az automatizálási fióknak a neve, amely a parancsmag által beadott változókat tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="4afe3-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afe3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afe3-119">-DefaultProfile</span></span>
<span data-ttu-id="4afe3-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="4afe3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4afe3-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4afe3-121">-Name</span></span>
<span data-ttu-id="4afe3-122">Annak a változónak a neve, amely a parancsmagot kapja.</span><span class="sxs-lookup"><span data-stu-id="4afe3-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4afe3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4afe3-123">-ResourceGroupName</span></span>
<span data-ttu-id="4afe3-124">Azt az erőforráscsoport-csoportot adja meg, amelyhez ez a parancsmag változókat kap.</span><span class="sxs-lookup"><span data-stu-id="4afe3-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afe3-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afe3-125">CommonParameters</span></span>
<span data-ttu-id="4afe3-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4afe3-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afe3-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afe3-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afe3-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afe3-128">INPUTS</span></span>

### <span data-ttu-id="4afe3-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="4afe3-129">None</span></span>
<span data-ttu-id="4afe3-130">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="4afe3-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4afe3-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4afe3-131">OUTPUTS</span></span>

### <span data-ttu-id="4afe3-132">Microsoft. Azure. Command. Automation. Model. változó</span><span class="sxs-lookup"><span data-stu-id="4afe3-132">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="4afe3-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4afe3-133">NOTES</span></span>

## <span data-ttu-id="4afe3-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4afe3-134">RELATED LINKS</span></span>

[<span data-ttu-id="4afe3-135">Új – AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4afe3-135">New-AzureRmAutomationVariable</span></span>](./New-AzureRMAutomationVariable.md)

[<span data-ttu-id="4afe3-136">Remove-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4afe3-136">Remove-AzureRmAutomationVariable</span></span>](./Remove-AzureRMAutomationVariable.md)

[<span data-ttu-id="4afe3-137">Set-AzureRmAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="4afe3-137">Set-AzureRmAutomationVariable</span></span>](./Set-AzureRMAutomationVariable.md)


