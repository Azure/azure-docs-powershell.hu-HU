---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
schema: 2.0.0
ms.openlocfilehash: 8559b8cdde324c3927ac835f49291441a4e58847
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/08/2020
ms.locfileid: "94016968"
---
# <span data-ttu-id="1ba33-101">Get-AzsNetworkAdminOverview</span><span class="sxs-lookup"><span data-stu-id="1ba33-101">Get-AzsNetworkAdminOverview</span></span>

## <span data-ttu-id="1ba33-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1ba33-102">SYNOPSIS</span></span>
<span data-ttu-id="1ba33-103">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="1ba33-103">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="1ba33-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1ba33-104">SYNTAX</span></span>

### <span data-ttu-id="1ba33-105">Get (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1ba33-105">Get (Default)</span></span>
```
Get-AzsNetworkAdminOverview [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1ba33-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1ba33-106">GetViaIdentity</span></span>
```
Get-AzsNetworkAdminOverview -InputObject <INetworkAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1ba33-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1ba33-107">DESCRIPTION</span></span>
<span data-ttu-id="1ba33-108">Áttekintés a hálózati erőforrás-szolgáltató állapotáról</span><span class="sxs-lookup"><span data-stu-id="1ba33-108">Get an overview of the state of the network resource provider.</span></span>

## <span data-ttu-id="1ba33-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1ba33-109">EXAMPLES</span></span>

### <span data-ttu-id="1ba33-110">--------------------------PÉLDA 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1ba33-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsNetworkAdminOverview
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsnetworkadminoverview
```



## <span data-ttu-id="1ba33-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1ba33-111">PARAMETERS</span></span>

### <span data-ttu-id="1ba33-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ba33-112">-DefaultProfile</span></span>
<span data-ttu-id="1ba33-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1ba33-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ba33-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ba33-114">-InputObject</span></span>
<span data-ttu-id="1ba33-115">Az Identity paraméter a kiépítéshez, a INPUTOBJECT tulajdonságainak megjegyzések szakasza, valamint a kivonatoló táblázat létrehozása című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ba33-115">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1ba33-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ba33-116">-SubscriptionId</span></span>
<span data-ttu-id="1ba33-117">Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1ba33-117">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1ba33-118">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1ba33-118">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1ba33-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ba33-119">CommonParameters</span></span>
<span data-ttu-id="1ba33-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1ba33-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ba33-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="1ba33-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ba33-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ba33-122">INPUTS</span></span>

### <span data-ttu-id="1ba33-123">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. models. INetworkAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1ba33-123">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.INetworkAdminIdentity</span></span>

## <span data-ttu-id="1ba33-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1ba33-124">OUTPUTS</span></span>

### <span data-ttu-id="1ba33-125">Microsoft. Azure. PowerShell. parancsmagok. NetworkAdmin. modellek. Api20150615. IAdminOverview</span><span class="sxs-lookup"><span data-stu-id="1ba33-125">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IAdminOverview</span></span>



## <span data-ttu-id="1ba33-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1ba33-126">NOTES</span></span>

<span data-ttu-id="1ba33-127">KOMPLEX paraméterek: az alábbi paraméterek létrehozásához készítse el a megfelelő tulajdonságokat tartalmazó hash-táblázatot.</span><span class="sxs-lookup"><span data-stu-id="1ba33-127">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1ba33-128">A hash-táblázatokról a Get-Help about_Hash_Tables futtatása című témakörben olvashat.</span><span class="sxs-lookup"><span data-stu-id="1ba33-128">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1ba33-129">INPUTOBJECT <INetworkAdminIdentity> : Identity paraméter</span><span class="sxs-lookup"><span data-stu-id="1ba33-129">INPUTOBJECT <INetworkAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1ba33-130">`[Id <String>]`: Erőforrás-identitás elérési útja</span><span class="sxs-lookup"><span data-stu-id="1ba33-130">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1ba33-131">`[Location <String>]`: Az erőforrás helye.</span><span class="sxs-lookup"><span data-stu-id="1ba33-131">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1ba33-132">`[ResourceName <String>]`: Az erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="1ba33-132">`[ResourceName <String>]`: Name of the resource.</span></span>
  - <span data-ttu-id="1ba33-133">`[SubscriptionId <String>]`: Az előfizetési hitelesítő adatok, amelyek egyedileg azonosíthatják a Microsoft Azure-előfizetést.</span><span class="sxs-lookup"><span data-stu-id="1ba33-133">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1ba33-134">Az előfizetési azonosító a minden szolgáltatási hívás URI-ja részét képezi.</span><span class="sxs-lookup"><span data-stu-id="1ba33-134">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="1ba33-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1ba33-135">RELATED LINKS</span></span>

