---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492043"
---
# <span data-ttu-id="d87e6-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d87e6-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="d87e6-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d87e6-102">SYNOPSIS</span></span>
<span data-ttu-id="d87e6-103">Az automatizálásból kapja a DSC konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="d87e6-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d87e6-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d87e6-104">SYNTAX</span></span>

### <span data-ttu-id="d87e6-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d87e6-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d87e6-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="d87e6-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d87e6-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d87e6-107">DESCRIPTION</span></span>
<span data-ttu-id="d87e6-108">A **Get-AzureRmAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak megfelelő (DSC) konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="d87e6-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="d87e6-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d87e6-109">EXAMPLES</span></span>

### <span data-ttu-id="d87e6-110">1. példa: az összes DSC-konfiguráció beolvasása</span><span class="sxs-lookup"><span data-stu-id="d87e6-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="d87e6-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC-konfigurációjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="d87e6-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="d87e6-112">2. példa: DSC-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="d87e6-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="d87e6-113">Ez a parancs a MyConfiguration nevű DSC-konfiguráció metaadatait kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="d87e6-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d87e6-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d87e6-114">PARAMETERS</span></span>

### <span data-ttu-id="d87e6-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d87e6-115">-AutomationAccountName</span></span>
<span data-ttu-id="d87e6-116">A parancsmag által beolvasott DSC-konfigurációt tartalmazó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="d87e6-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d87e6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d87e6-117">-DefaultProfile</span></span>
<span data-ttu-id="d87e6-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="d87e6-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d87e6-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="d87e6-119">-Name</span></span>
<span data-ttu-id="d87e6-120">Annak a DSC-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="d87e6-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="d87e6-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d87e6-121">-ResourceGroupName</span></span>
<span data-ttu-id="d87e6-122">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="d87e6-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="d87e6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d87e6-123">CommonParameters</span></span>
<span data-ttu-id="d87e6-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d87e6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d87e6-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d87e6-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d87e6-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d87e6-126">INPUTS</span></span>

### <span data-ttu-id="d87e6-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d87e6-127">System.String</span></span>

## <span data-ttu-id="d87e6-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d87e6-128">OUTPUTS</span></span>

### <span data-ttu-id="d87e6-129">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d87e6-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="d87e6-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d87e6-130">NOTES</span></span>

## <span data-ttu-id="d87e6-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d87e6-131">RELATED LINKS</span></span>

[<span data-ttu-id="d87e6-132">Exportálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d87e6-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="d87e6-133">Importálás – AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="d87e6-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


