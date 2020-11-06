---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497979"
---
# <span data-ttu-id="53953-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="53953-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="53953-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="53953-102">SYNOPSIS</span></span>
<span data-ttu-id="53953-103">Metaadatokat kap a modulokhoz az automatizálásból.</span><span class="sxs-lookup"><span data-stu-id="53953-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53953-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="53953-104">SYNTAX</span></span>

### <span data-ttu-id="53953-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="53953-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53953-106">ByName</span><span class="sxs-lookup"><span data-stu-id="53953-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53953-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="53953-107">DESCRIPTION</span></span>
<span data-ttu-id="53953-108">A **Get-AzureRmAutomationModule** parancsmag metaadatokat kap az Azure automatizálási modulokból.</span><span class="sxs-lookup"><span data-stu-id="53953-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="53953-109">Példák</span><span class="sxs-lookup"><span data-stu-id="53953-109">EXAMPLES</span></span>

### <span data-ttu-id="53953-110">Példa 1: az összes modul beolvasása</span><span class="sxs-lookup"><span data-stu-id="53953-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="53953-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes modulját megkapja.</span><span class="sxs-lookup"><span data-stu-id="53953-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="53953-112">2. példa: modul beszerzése</span><span class="sxs-lookup"><span data-stu-id="53953-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="53953-113">Ez a parancs egy ContosoModule nevű modult kap a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="53953-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="53953-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="53953-114">PARAMETERS</span></span>

### <span data-ttu-id="53953-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="53953-115">-AutomationAccountName</span></span>
<span data-ttu-id="53953-116">Annak az automatizálási fióknak a neve, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="53953-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="53953-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="53953-117">-Name</span></span>
<span data-ttu-id="53953-118">Annak a modulnak a neve, amelyhez a parancsmag metaadatot kap.</span><span class="sxs-lookup"><span data-stu-id="53953-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="53953-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53953-119">-ResourceGroupName</span></span>
<span data-ttu-id="53953-120">Annak a csoportnak a nevét adja meg, amelyhez ez a parancsmag a modul metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="53953-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="53953-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53953-121">-DefaultProfile</span></span>
<span data-ttu-id="53953-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="53953-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53953-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53953-123">CommonParameters</span></span>
<span data-ttu-id="53953-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="53953-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53953-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53953-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53953-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="53953-126">INPUTS</span></span>

## <span data-ttu-id="53953-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="53953-127">OUTPUTS</span></span>

### <span data-ttu-id="53953-128">Microsoft. Azure. Command. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="53953-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="53953-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="53953-129">NOTES</span></span>

## <span data-ttu-id="53953-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="53953-130">RELATED LINKS</span></span>

[<span data-ttu-id="53953-131">Új – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="53953-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="53953-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="53953-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="53953-133">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="53953-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


