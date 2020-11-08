---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186130"
---
# <span data-ttu-id="0a699-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a699-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="0a699-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0a699-102">SYNOPSIS</span></span>
<span data-ttu-id="0a699-103">Az automatizálásból kapja a DSC konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="0a699-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="0a699-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0a699-104">SYNTAX</span></span>

### <span data-ttu-id="0a699-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0a699-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a699-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0a699-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a699-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="0a699-107">DESCRIPTION</span></span>
<span data-ttu-id="0a699-108">A **Get-AzAutomationDscConfiguration** parancsmag az Azure automatizálási beállításainak megfelelő (DSC) konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="0a699-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="0a699-109">Példák</span><span class="sxs-lookup"><span data-stu-id="0a699-109">EXAMPLES</span></span>

### <span data-ttu-id="0a699-110">1. példa: az összes DSC-konfiguráció beolvasása</span><span class="sxs-lookup"><span data-stu-id="0a699-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0a699-111">Ez a parancs a Contoso17 nevű automatizálási fiók összes DSC-konfigurációjának metaadatait kapja.</span><span class="sxs-lookup"><span data-stu-id="0a699-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0a699-112">2. példa: DSC-konfiguráció beszerzése név alapján</span><span class="sxs-lookup"><span data-stu-id="0a699-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="0a699-113">Ez a parancs a MyConfiguration nevű DSC-konfiguráció metaadatait kapja meg a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="0a699-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0a699-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0a699-114">PARAMETERS</span></span>

### <span data-ttu-id="0a699-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a699-115">-AutomationAccountName</span></span>
<span data-ttu-id="0a699-116">A parancsmag által beolvasott DSC-konfigurációt tartalmazó automatizálási fiók nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="0a699-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a699-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a699-117">-DefaultProfile</span></span>
<span data-ttu-id="0a699-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="0a699-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a699-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="0a699-119">-Name</span></span>
<span data-ttu-id="0a699-120">Annak a DSC-konfigurációnak a nevét adja meg, amelyre a parancsmag bekerül.</span><span class="sxs-lookup"><span data-stu-id="0a699-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="0a699-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a699-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a699-122">Annak a csoportnak a neve, amelyhez ez a parancsmag DSC-konfigurációt kap.</span><span class="sxs-lookup"><span data-stu-id="0a699-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="0a699-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a699-123">CommonParameters</span></span>
<span data-ttu-id="0a699-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0a699-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a699-125">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a699-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a699-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a699-126">INPUTS</span></span>

### <span data-ttu-id="0a699-127">System. String</span><span class="sxs-lookup"><span data-stu-id="0a699-127">System.String</span></span>

## <span data-ttu-id="0a699-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0a699-128">OUTPUTS</span></span>

### <span data-ttu-id="0a699-129">Microsoft. Azure. Command. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a699-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="0a699-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0a699-130">NOTES</span></span>

## <span data-ttu-id="0a699-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0a699-131">RELATED LINKS</span></span>

[<span data-ttu-id="0a699-132">Exportálás – AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a699-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="0a699-133">Importálás – AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="0a699-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


