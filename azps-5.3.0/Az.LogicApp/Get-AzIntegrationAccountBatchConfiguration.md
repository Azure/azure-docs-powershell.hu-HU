---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98480075"
---
# <span data-ttu-id="c4126-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4126-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c4126-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4126-102">SYNOPSIS</span></span>
<span data-ttu-id="c4126-103">Integrációs fiók köteg-konfigurációját kapja.</span><span class="sxs-lookup"><span data-stu-id="c4126-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="c4126-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c4126-104">SYNTAX</span></span>

### <span data-ttu-id="c4126-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c4126-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4126-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c4126-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4126-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c4126-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4126-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c4126-108">DESCRIPTION</span></span>
<span data-ttu-id="c4126-109">A **Get-AzIntegrationAccountBatchConfiguration** parancsmag egy kötegkonfigurációt kap egy integrációs fiókból.</span><span class="sxs-lookup"><span data-stu-id="c4126-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="c4126-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c4126-110">EXAMPLES</span></span>

### <span data-ttu-id="c4126-111">1. példa: Köteg konfigurálása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="c4126-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c4126-112">Egy "sampleBatchConfig" nevű kötegkonfigurációt a "sampleIntegrationAccount" integrációs fiókban talál, amely a "sampleResourceGroup" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="c4126-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="c4126-113">2. példa: Az integrációs fiók összes kötegkonfigurációjának felsorolása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="c4126-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig2
Name       : sampleBatchConfig2
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="c4126-114">Az "sampleResourceGroup" erőforráscsoportban található "sampleIntegrationAccount" integrációs fiókban található összes kötegkonfiguráció lekérte.</span><span class="sxs-lookup"><span data-stu-id="c4126-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="c4126-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4126-115">PARAMETERS</span></span>

### <span data-ttu-id="c4126-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4126-116">-DefaultProfile</span></span>
<span data-ttu-id="c4126-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c4126-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4126-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c4126-118">-Name</span></span>
<span data-ttu-id="c4126-119">Az integrációs fiók kötegkonfigurációs neve.</span><span class="sxs-lookup"><span data-stu-id="c4126-119">The integration account batch configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchConfigurationName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4126-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="c4126-120">-ParentName</span></span>
<span data-ttu-id="c4126-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="c4126-121">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases: IntegrationAccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4126-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c4126-122">-ParentObject</span></span>
<span data-ttu-id="c4126-123">Egy integrációs fiókobjektum.</span><span class="sxs-lookup"><span data-stu-id="c4126-123">An integration account object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Logic.Models.IntegrationAccount
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4126-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="c4126-124">-ParentResourceId</span></span>
<span data-ttu-id="c4126-125">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="c4126-125">The integration account resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c4126-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4126-126">-ResourceGroupName</span></span>
<span data-ttu-id="c4126-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c4126-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationAccount
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4126-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4126-128">CommonParameters</span></span>
<span data-ttu-id="c4126-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4126-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4126-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4126-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4126-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4126-131">INPUTS</span></span>

### <span data-ttu-id="c4126-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="c4126-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="c4126-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4126-133">System.String</span></span>

## <span data-ttu-id="c4126-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c4126-134">OUTPUTS</span></span>

### <span data-ttu-id="c4126-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="c4126-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="c4126-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c4126-136">NOTES</span></span>

## <span data-ttu-id="c4126-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c4126-137">RELATED LINKS</span></span>
