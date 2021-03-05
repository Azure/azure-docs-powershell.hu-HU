---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountassembly
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountAssembly.md
ms.openlocfilehash: 95daa8025dde470e85d0e00e09c00f26d08e1342
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007798"
---
# <span data-ttu-id="efd01-101">Get-AzIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="efd01-101">Get-AzIntegrationAccountAssembly</span></span>

## <span data-ttu-id="efd01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd01-102">SYNOPSIS</span></span>
<span data-ttu-id="efd01-103">Integrációs fiók összeállítása.</span><span class="sxs-lookup"><span data-stu-id="efd01-103">Gets an integration account assembly.</span></span>

## <span data-ttu-id="efd01-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="efd01-104">SYNTAX</span></span>

### <span data-ttu-id="efd01-105">ByIntegrationAccount (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="efd01-105">ByIntegrationAccount (Default)</span></span>
```
Get-AzIntegrationAccountAssembly -ResourceGroupName <String> -ParentName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efd01-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="efd01-106">ByInputObject</span></span>
```
Get-AzIntegrationAccountAssembly -ParentObject <IntegrationAccount> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efd01-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="efd01-107">ByResourceId</span></span>
```
Get-AzIntegrationAccountAssembly -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efd01-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="efd01-108">DESCRIPTION</span></span>
<span data-ttu-id="efd01-109">A **Get-AzIntegrationAccountAssembly** parancsmag egy integrációs fiókból kap egy szerelvényt.</span><span class="sxs-lookup"><span data-stu-id="efd01-109">The **Get-AzIntegrationAccountAssembly** cmdlet gets an assembly from an integration account.</span></span>

## <span data-ttu-id="efd01-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="efd01-110">EXAMPLES</span></span>

### <span data-ttu-id="efd01-111">1. példa: Szerelvény lekérte paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="efd01-111">Example 1: Get an assembly by parameters</span></span>
```powershell
PS C:\> Get-AzIntegrationAccountAssembly -ResourceGroupName "sampleResourceGroup" -IntegrationAccountName "sampleIntegrationAccount" -AssemblyName "sampleAssembly"

Properties : Microsoft.Azure.Management.Logic.Models.AssemblyProperties
Id         : /subscriptions/{SubscriptionId}/resourceGroups/sampleResourceGroup/providers/Microsoft.Logic/integrationAccounts/sampleIntegrationAccount/assemblies/sampleAssembly
Name       : sampleAssembly
Type       : Microsoft.Logic/integrationAccounts/assemblies
Location   :
Tags       :

```

<span data-ttu-id="efd01-112">Szerezze be a "sampleAssembly" nevű szerelvényt az "sampleIntegrationAccount" integrációs fiókban, amely a "sampleResourceGroup" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="efd01-112">Get an assembly named "sampleAssembly" located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

### <span data-ttu-id="efd01-113">2. példa: Az integrációs fiók összes szerelvényének felsorolása paraméterek alapján</span><span class="sxs-lookup"><span data-stu-id="efd01-113">Example 2: List all assemblies in an integration account by parameters</span></span>
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

<span data-ttu-id="efd01-114">Szerezze be a "sampleIntegrationAccount" integrációs fiókban található összes összeállítást, amely a "sampleResourceGroup" erőforráscsoportban található.</span><span class="sxs-lookup"><span data-stu-id="efd01-114">Get all assemblies located in the integration account "sampleIntegrationAccount" which is contained in the resource group "sampleResourceGroup".</span></span>

## <span data-ttu-id="efd01-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="efd01-115">PARAMETERS</span></span>

### <span data-ttu-id="efd01-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd01-116">-DefaultProfile</span></span>
<span data-ttu-id="efd01-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="efd01-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd01-118">-Name</span><span class="sxs-lookup"><span data-stu-id="efd01-118">-Name</span></span>
<span data-ttu-id="efd01-119">Az integrációs fiók szerelvényének neve.</span><span class="sxs-lookup"><span data-stu-id="efd01-119">The integration account assembly name.</span></span>

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

### <span data-ttu-id="efd01-120">-ParentName</span><span class="sxs-lookup"><span data-stu-id="efd01-120">-ParentName</span></span>
<span data-ttu-id="efd01-121">Az integrációs fiók neve.</span><span class="sxs-lookup"><span data-stu-id="efd01-121">The integration account name.</span></span>

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

### <span data-ttu-id="efd01-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="efd01-122">-ParentObject</span></span>
<span data-ttu-id="efd01-123">Egy integrációs fiókobjektum.</span><span class="sxs-lookup"><span data-stu-id="efd01-123">An integration account object.</span></span>

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

### <span data-ttu-id="efd01-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="efd01-124">-ParentResourceId</span></span>
<span data-ttu-id="efd01-125">Az integrációs fiók erőforrás-azonosítója.</span><span class="sxs-lookup"><span data-stu-id="efd01-125">The integration account resource id.</span></span>

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

### <span data-ttu-id="efd01-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efd01-126">-ResourceGroupName</span></span>
<span data-ttu-id="efd01-127">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="efd01-127">The resource group name.</span></span>

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

### <span data-ttu-id="efd01-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd01-128">CommonParameters</span></span>
<span data-ttu-id="efd01-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efd01-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd01-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efd01-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd01-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="efd01-131">INPUTS</span></span>

### <span data-ttu-id="efd01-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="efd01-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

### <span data-ttu-id="efd01-133">System.String</span><span class="sxs-lookup"><span data-stu-id="efd01-133">System.String</span></span>

## <span data-ttu-id="efd01-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="efd01-134">OUTPUTS</span></span>

### <span data-ttu-id="efd01-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span><span class="sxs-lookup"><span data-stu-id="efd01-135">Microsoft.Azure.Commands.LogicApp.Models.PSIntegrationAccountAssembly</span></span>

## <span data-ttu-id="efd01-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="efd01-136">NOTES</span></span>

## <span data-ttu-id="efd01-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="efd01-137">RELATED LINKS</span></span>
