---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/get-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Get-AzConnectedMachineExtension.md
ms.openlocfilehash: ce7069b0da8e4bb4c8526f235d7cc7cd9b481e87
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194450"
---
# <span data-ttu-id="c568c-101">Get-AzConnectedMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c568c-101">Get-AzConnectedMachineExtension</span></span>

## <span data-ttu-id="c568c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="c568c-102">SYNOPSIS</span></span>
<span data-ttu-id="c568c-103">A bővítmény eléréséhez használandó művelet</span><span class="sxs-lookup"><span data-stu-id="c568c-103">The operation to get the extension.</span></span>

## <span data-ttu-id="c568c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="c568c-104">SYNTAX</span></span>

### <span data-ttu-id="c568c-105">Lista (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c568c-105">List (Default)</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-Expand <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c568c-106">Beszerzése</span><span class="sxs-lookup"><span data-stu-id="c568c-106">Get</span></span>
```
Get-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c568c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="c568c-107">DESCRIPTION</span></span>
<span data-ttu-id="c568c-108">A bővítmény eléréséhez használandó művelet</span><span class="sxs-lookup"><span data-stu-id="c568c-108">The operation to get the extension.</span></span>

## <span data-ttu-id="c568c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="c568c-109">EXAMPLES</span></span>

### <span data-ttu-id="c568c-110">Példa 1: egy gép összes bővítményének listázása</span><span class="sxs-lookup"><span data-stu-id="c568c-110">Example 1: List all extensions for a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2

Name    Location  PropertiesType        ProvisioningState
----    --------  --------------        -----------------
custom  westus2   CustomScriptExtension Succeeded
custom  westus2   CustomScriptExtension Succeeded
dsc     westus2   DSC                   Succeeded
```

<span data-ttu-id="c568c-111">Egy adott gép összes bővítményének listázása.</span><span class="sxs-lookup"><span data-stu-id="c568c-111">Lists all extensions for a specific machine.</span></span>

### <span data-ttu-id="c568c-112">2. példa: adott bővítmény beszerzése a számítógépen</span><span class="sxs-lookup"><span data-stu-id="c568c-112">Example 2: Get a specific extension on a machine</span></span>
```powershell
PS C:\> Get-AzConnectedMachineExtension -ResourceGroupName contoso-connected-machines -MachineName winwestus2_2 -Name dsc

Name  Location  PropertiesType        ProvisioningState
----  --------  --------------        -----------------
dsc   westus2   CustomScriptExtension Succeeded
```

<span data-ttu-id="c568c-113">Meghatározott bővítményt kap a számítógépen.</span><span class="sxs-lookup"><span data-stu-id="c568c-113">Gets a specific extension on a machine.</span></span>

## <span data-ttu-id="c568c-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="c568c-114">PARAMETERS</span></span>

### <span data-ttu-id="c568c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c568c-115">-DefaultProfile</span></span>
<span data-ttu-id="c568c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c568c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c568c-117">– Kibontás</span><span class="sxs-lookup"><span data-stu-id="c568c-117">-Expand</span></span>
<span data-ttu-id="c568c-118">A művelethez alkalmazni kívánt kifejezés kibontása.</span><span class="sxs-lookup"><span data-stu-id="c568c-118">The expand expression to apply on the operation.</span></span>

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

### <span data-ttu-id="c568c-119">-Számítógépnév</span><span class="sxs-lookup"><span data-stu-id="c568c-119">-MachineName</span></span>
<span data-ttu-id="c568c-120">Annak a gépnek a neve, amely a kiterjesztést tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="c568c-120">The name of the machine containing the extension.</span></span>

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

### <span data-ttu-id="c568c-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="c568c-121">-Name</span></span>
<span data-ttu-id="c568c-122">A gép mellékének neve.</span><span class="sxs-lookup"><span data-stu-id="c568c-122">The name of the machine extension.</span></span>

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

### <span data-ttu-id="c568c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c568c-123">-ResourceGroupName</span></span>
<span data-ttu-id="c568c-124">Az erőforráscsoport neve.</span><span class="sxs-lookup"><span data-stu-id="c568c-124">The name of the resource group.</span></span>

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

### <span data-ttu-id="c568c-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c568c-125">-SubscriptionId</span></span>
<span data-ttu-id="c568c-126">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="c568c-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c568c-127">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="c568c-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c568c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c568c-128">CommonParameters</span></span>
<span data-ttu-id="c568c-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="c568c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c568c-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="c568c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c568c-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="c568c-131">INPUTS</span></span>

## <span data-ttu-id="c568c-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c568c-132">OUTPUTS</span></span>

### <span data-ttu-id="c568c-133">Microsoft. Azure. PowerShell. parancsmagok. ConnectedMachine. modellek. Api20200802. IMachineExtension</span><span class="sxs-lookup"><span data-stu-id="c568c-133">Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension</span></span>

## <span data-ttu-id="c568c-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="c568c-134">NOTES</span></span>

<span data-ttu-id="c568c-135">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="c568c-135">ALIASES</span></span>

## <span data-ttu-id="c568c-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c568c-136">RELATED LINKS</span></span>
