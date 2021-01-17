---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: 0616cb9f2a379e93a01b450ab8a66da95ca9add1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98478745"
---
# <span data-ttu-id="57e0b-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e0b-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="57e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="57e0b-103">DSC-konfigurációkat kap az automatizálástól.</span><span class="sxs-lookup"><span data-stu-id="57e0b-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="57e0b-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="57e0b-104">SYNTAX</span></span>

### <span data-ttu-id="57e0b-105">ByAll (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="57e0b-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57e0b-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="57e0b-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="57e0b-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="57e0b-107">DESCRIPTION</span></span>
<span data-ttu-id="57e0b-108">A **Get-AzAutomationDscConfiguration** parancsmag az APS-hez szükséges államkonfigurációs (DSC) konfigurációkat kap az Azure Automationtől.</span><span class="sxs-lookup"><span data-stu-id="57e0b-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="57e0b-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="57e0b-109">EXAMPLES</span></span>

### <span data-ttu-id="57e0b-110">1. példa: Az összes DSC-konfiguráció lekérte</span><span class="sxs-lookup"><span data-stu-id="57e0b-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="57e0b-111">Ez a parancs metaadatokat kap a Contoso17 nevű automatizálási fiók összes DSC-konfigurációjában.</span><span class="sxs-lookup"><span data-stu-id="57e0b-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="57e0b-112">2. példa: DSC-konfiguráció beállítása név szerint</span><span class="sxs-lookup"><span data-stu-id="57e0b-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="57e0b-113">Ez a parancs metaadatokat kap egy MyConfiguration nevű DSC-konfigurációhoz a Contoso17 nevű automatizálási fiókban.</span><span class="sxs-lookup"><span data-stu-id="57e0b-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="57e0b-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="57e0b-114">PARAMETERS</span></span>

### <span data-ttu-id="57e0b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="57e0b-115">-AutomationAccountName</span></span>
<span data-ttu-id="57e0b-116">Annak az automatizálási fióknak a nevét adja meg, amely a parancsmag DSC-konfigurációit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="57e0b-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57e0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57e0b-117">-DefaultProfile</span></span>
<span data-ttu-id="57e0b-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="57e0b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="57e0b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="57e0b-119">-Name</span></span>
<span data-ttu-id="57e0b-120">A parancsmag DSC-konfigurációjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57e0b-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="57e0b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57e0b-121">-ResourceGroupName</span></span>
<span data-ttu-id="57e0b-122">Annak az erőforráscsoportnak a nevét adja meg, amelynek a parancsmagja DSC-konfigurációkat kap.</span><span class="sxs-lookup"><span data-stu-id="57e0b-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="57e0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57e0b-123">CommonParameters</span></span>
<span data-ttu-id="57e0b-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57e0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57e0b-125">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57e0b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57e0b-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="57e0b-126">INPUTS</span></span>

### <span data-ttu-id="57e0b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="57e0b-127">System.String</span></span>

## <span data-ttu-id="57e0b-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57e0b-128">OUTPUTS</span></span>

### <span data-ttu-id="57e0b-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e0b-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="57e0b-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="57e0b-130">NOTES</span></span>

## <span data-ttu-id="57e0b-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57e0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="57e0b-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e0b-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="57e0b-133">Import-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="57e0b-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


