---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: 423834d0dc7a324743795e0d54324a51f1cd04ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012405"
---
# <span data-ttu-id="5a7ef-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5a7ef-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="5a7ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="5a7ef-103">A bővítmény lekért művelete.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-103">The operation to get the extension.</span></span>

## <span data-ttu-id="5a7ef-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5a7ef-104">SYNTAX</span></span>

### <span data-ttu-id="5a7ef-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5a7ef-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5a7ef-106">Bej.le</span><span class="sxs-lookup"><span data-stu-id="5a7ef-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="5a7ef-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5a7ef-107">DESCRIPTION</span></span>
<span data-ttu-id="5a7ef-108">A bővítmény lekért művelete.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-108">The operation to get the extension.</span></span>

## <span data-ttu-id="5a7ef-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5a7ef-109">EXAMPLES</span></span>

### <span data-ttu-id="5a7ef-110">1. példa: A gép összes bővítményének felsorolása</span><span class="sxs-lookup"><span data-stu-id="5a7ef-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="5a7ef-111">Egy adott gép összes bővítményét felsorolja.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="5a7ef-112">2. példa: Adott bővítmény lekérte egy gépre</span><span class="sxs-lookup"><span data-stu-id="5a7ef-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="5a7ef-113">Egy adott bővítményt kap a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="5a7ef-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a7ef-114">PARAMETERS</span></span>

### <span data-ttu-id="5a7ef-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a7ef-115">-DefaultProfile</span></span>
<span data-ttu-id="5a7ef-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-117">-Kibontás</span><span class="sxs-lookup"><span data-stu-id="5a7ef-117">-Expand</span></span>
<span data-ttu-id="5a7ef-118">A műveletre alkalmazandó kibontó kifejezés.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-118">The expand expression to apply on the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-119">-MachineName</span><span class="sxs-lookup"><span data-stu-id="5a7ef-119">-MachineName</span></span>
<span data-ttu-id="5a7ef-120">A bővítményt tartalmazó gép neve.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-120">The name of the machine containing the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5a7ef-121">-Name</span></span>
<span data-ttu-id="5a7ef-122">A gépbővítmény neve.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-122">The name of the machine extension.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a7ef-123">-ResourceGroupName</span></span>
<span data-ttu-id="5a7ef-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-124">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5a7ef-125">-SubscriptionId</span></span>
<span data-ttu-id="5a7ef-126">Előfizetési hitelesítő adatok, amelyek egyedileg azonosítják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5a7ef-127">Az előfizetésazonosító minden szolgáltatási hívás URI-jának részét képezi.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a7ef-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a7ef-128">CommonParameters</span></span>
<span data-ttu-id="5a7ef-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a7ef-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a7ef-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5a7ef-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a7ef-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5a7ef-131">INPUTS</span></span>

## <span data-ttu-id="5a7ef-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5a7ef-132">OUTPUTS</span></span>

### <span data-ttu-id="5a7ef-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="5a7ef-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="5a7ef-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5a7ef-134">NOTES</span></span>

<span data-ttu-id="5a7ef-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="5a7ef-135">ALIASES</span></span>

## <span data-ttu-id="5a7ef-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5a7ef-136">RELATED LINKS</span></span>

