---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 4ac549e53054d0650c0e64e45c662c6b184067b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499268"
---
# <span data-ttu-id="1d53a-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d53a-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="1d53a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1d53a-102">SYNOPSIS</span></span>
<span data-ttu-id="1d53a-103">Az automatizálásból kapja a DSC konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="1d53a-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d53a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1d53a-104">SYNTAX</span></span>

### <span data-ttu-id="1d53a-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1d53a-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d53a-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1d53a-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d53a-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1d53a-107">DESCRIPTION</span></span>
<span data-ttu-id="1d53a-108">A **Get-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak megfelelő (DSC) konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="1d53a-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="1d53a-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1d53a-109">EXAMPLES</span></span>

### <span data-ttu-id="1d53a-110">1. példa: az összes DSC-konfiguráció beolvasása</span><span class="sxs-lookup"><span data-stu-id="1d53a-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="1d53a-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC-konfigurációjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="1d53a-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="1d53a-112">2. példa: DSC-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="1d53a-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="1d53a-113">Ez a parancs a MyConfiguration nevű DSC-konfiguráció metaadatait kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="1d53a-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d53a-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1d53a-114">PARAMETERS</span></span>

### <span data-ttu-id="1d53a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d53a-115">-AutomationAccountName</span></span>
<span data-ttu-id="1d53a-116">A parancsmag által beolvasott DSC-konfigurációt tartalmazó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="1d53a-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1d53a-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="1d53a-117">-Name</span></span>
<span data-ttu-id="1d53a-118">Annak a DSC-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="1d53a-118">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d53a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d53a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1d53a-120">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="1d53a-120">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="1d53a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d53a-121">-DefaultProfile</span></span>
<span data-ttu-id="1d53a-122">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1d53a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d53a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d53a-123">CommonParameters</span></span>
<span data-ttu-id="1d53a-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1d53a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d53a-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d53a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d53a-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d53a-126">INPUTS</span></span>

## <span data-ttu-id="1d53a-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1d53a-127">OUTPUTS</span></span>

### <span data-ttu-id="1d53a-128">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d53a-128">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="1d53a-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1d53a-129">NOTES</span></span>

## <span data-ttu-id="1d53a-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1d53a-130">RELATED LINKS</span></span>

[<span data-ttu-id="1d53a-131">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d53a-131">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="1d53a-132">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d53a-132">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


