---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountbatchconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountBatchConfiguration.md
ms.openlocfilehash: 26a2e414f05fc0aeb209afa946ae168c59ea4ff8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846010"
---
# <span data-ttu-id="10d66-101">Get-AzIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10d66-101">Get-AzIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="10d66-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="10d66-102">SYNOPSIS</span></span>
<span data-ttu-id="10d66-103">Megkapja az integrációs fiók kötegének konfigurációját.</span><span class="sxs-lookup"><span data-stu-id="10d66-103">Gets an integration account batch configuration.</span></span>

## <span data-ttu-id="10d66-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="10d66-104">SYNTAX</span></span>

### <span data-ttu-id="10d66-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="10d66-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d66-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="10d66-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d66-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="10d66-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountBatchConfiguration -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10d66-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="10d66-108">DESCRIPTION</span></span>
<span data-ttu-id="10d66-109">A **Get-AzIntegrationAccountBatchConfiguration** parancsmag az integrációs fiókból kapja meg a köteg konfigurációt.</span><span class="sxs-lookup"><span data-stu-id="10d66-109">The **Get-AzIntegrationAccountBatchConfiguration** cmdlet gets an batch configuration from an integration account.</span></span>

## <span data-ttu-id="10d66-110">Példák</span><span class="sxs-lookup"><span data-stu-id="10d66-110">EXAMPLES</span></span>

### <span data-ttu-id="10d66-111">Példa 1: kötegfájl-konfiguráció beszerzése paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="10d66-111">Example 1: Get a batch configuration by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountBatchConfiguration -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -BatchConfigurationName "sampleBatchConfig"

Properties : Microsoft.Azure.Management.Logic.Models.BatchConfigurationProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/batchConfigurations/sampleBatchConfig
Name       : sampleBatchConfig
Type       : Microsoft.Logic/integrationAccounts/batchConfigurations
Location   :
Tags       :

```

<span data-ttu-id="10d66-112">Beszerezhet egy "sampleBatchConfig" nevű köteg-konfigurációt, amely az "sampleIntegrationAccount" erőforráscsoport "sampleResourceGroup" erőforráscsoporthoz tartozó "" nevű integrációs fiókban található.</span><span class="sxs-lookup"><span data-stu-id="10d66-112">Get a batch configuration named "sampleBatchConfig" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="10d66-113">2. példa: az integrációs fiók minden köteg-konfigurációjának listázása paraméterek szerint</span><span class="sxs-lookup"><span data-stu-id="10d66-113">Example 2: List all batch configurations in an integration account by parameters</span></span>
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

<span data-ttu-id="10d66-114">Az integrációs fiók "sampleIntegrationAccount" ("sampleResourceGroup") erőforráscsoporthoz tartozó összes kötegfájl-konfiguráció beszerzése.</span><span class="sxs-lookup"><span data-stu-id="10d66-114">Get all batch configurations located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="10d66-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="10d66-115">PARAMETERS</span></span>

### <span data-ttu-id="10d66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d66-116">-DefaultProfile</span></span>
<span data-ttu-id="10d66-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="10d66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d66-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="10d66-118">-Name</span></span>
<span data-ttu-id="10d66-119">Az integrációs fiók kötegének neve.</span><span class="sxs-lookup"><span data-stu-id="10d66-119">The integration account batch configuration name.</span></span>

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

### <span data-ttu-id="10d66-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="10d66-120">-ParentName</span></span>
<span data-ttu-id="10d66-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="10d66-121">The integration account name.</span></span>

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

### <span data-ttu-id="10d66-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="10d66-122">-ParentObject</span></span>
<span data-ttu-id="10d66-123">Az integrációs fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="10d66-123">An integration account object.</span></span>

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

### <span data-ttu-id="10d66-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="10d66-124">-ParentResourceId</span></span>
<span data-ttu-id="10d66-125">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="10d66-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="10d66-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d66-126">-ResourceGroupName</span></span>
<span data-ttu-id="10d66-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="10d66-127">The resource group name.</span></span>

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

### <span data-ttu-id="10d66-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d66-128">CommonParameters</span></span>
<span data-ttu-id="10d66-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="10d66-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d66-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d66-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d66-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="10d66-131">INPUTS</span></span>

### <span data-ttu-id="10d66-132">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="10d66-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="10d66-133">System. String</span><span class="sxs-lookup"><span data-stu-id="10d66-133">System.String</span></span>

## <span data-ttu-id="10d66-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="10d66-134">OUTPUTS</span></span>

### <span data-ttu-id="10d66-135">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountBatchConfiguration</span><span class="sxs-lookup"><span data-stu-id="10d66-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountBatchConfiguration</span></span>

## <span data-ttu-id="10d66-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="10d66-136">NOTES</span></span>

## <span data-ttu-id="10d66-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="10d66-137">RELATED LINKS</span></span>
