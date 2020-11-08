---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 59b4ad9eb439808033233aa1677be16862c8a973
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194369"
---
# <span data-ttu-id="a9ef8-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a9ef8-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a9ef8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a9ef8-102">SYNOPSIS</span></span>
<span data-ttu-id="a9ef8-103">Megkapja az integrációs fiók kódösszeállítását.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="a9ef8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a9ef8-104">SYNTAX</span></span>

### <span data-ttu-id="a9ef8-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a9ef8-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ef8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a9ef8-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9ef8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ef8-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9ef8-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="a9ef8-108">DESCRIPTION</span></span>
<span data-ttu-id="a9ef8-109">A **Get-AzIntegrationAccountAssembly** parancsmag egy integrációs fiókból kapja meg a kódösszeállítást.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="a9ef8-110">Példák</span><span class="sxs-lookup"><span data-stu-id="a9ef8-110">EXAMPLES</span></span>

### <span data-ttu-id="a9ef8-111">Példa 1: kódösszeállítás beszerzése paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="a9ef8-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a9ef8-112">Beszerezhet egy "sampleAssembly" nevű kódösszeállítást az "sampleIntegrationAccount" erőforráscsoport "sampleResourceGroup" erőforráscsoporthoz tartozó "" nevű integrációs fiókban.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="a9ef8-113">2. példa: az integrációs fiók összes összeállításának felsorolása paraméterek szerint</span><span class="sxs-lookup"><span data-stu-id="a9ef8-113">Example 2: List all assemblies in an integration account by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly2
Name       : sampleAssembly2
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="a9ef8-114">Az "sampleIntegrationAccount" ("sampleResourceGroup") erőforráscsoport az integrációs fiókban található összes kódösszeállítás beolvasása.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="a9ef8-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a9ef8-115">PARAMETERS</span></span>

### <span data-ttu-id="a9ef8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9ef8-116">-DefaultProfile</span></span>
<span data-ttu-id="a9ef8-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9ef8-118">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="a9ef8-118">-Name</span></span>
<span data-ttu-id="a9ef8-119">Az integrációs fiók kódösszeállításának neve.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-119">The integration account assembly name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssemblyName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9ef8-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="a9ef8-120">-ParentName</span></span>
<span data-ttu-id="a9ef8-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-121">The integration account name.</span></span>

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

### <span data-ttu-id="a9ef8-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a9ef8-122">-ParentObject</span></span>
<span data-ttu-id="a9ef8-123">Az integrációs fiók objektuma.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-123">An integration account object.</span></span>

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

### <span data-ttu-id="a9ef8-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a9ef8-124">-ParentResourceId</span></span>
<span data-ttu-id="a9ef8-125">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="a9ef8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9ef8-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9ef8-127">Az erőforrás csoport neve.</span><span class="sxs-lookup"><span data-stu-id="a9ef8-127">The resource group name.</span></span>

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

### <span data-ttu-id="a9ef8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9ef8-128">CommonParameters</span></span>
<span data-ttu-id="a9ef8-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a9ef8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9ef8-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9ef8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9ef8-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9ef8-131">INPUTS</span></span>

### <span data-ttu-id="a9ef8-132">Microsoft. Azure. Management. Logic. models. IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="a9ef8-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="a9ef8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a9ef8-133">System.String</span></span>

## <span data-ttu-id="a9ef8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a9ef8-134">OUTPUTS</span></span>

### <span data-ttu-id="a9ef8-135">Microsoft. Azure. Command. LogicApp. models. PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="a9ef8-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="a9ef8-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a9ef8-136">NOTES</span></span>

## <span data-ttu-id="a9ef8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a9ef8-137">RELATED LINKS</span></span>
