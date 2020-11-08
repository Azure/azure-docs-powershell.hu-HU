---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194580"
---
# <span data-ttu-id="8d2bc-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="8d2bc-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="8d2bc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8d2bc-102">SYNOPSIS</span></span>
<span data-ttu-id="8d2bc-103">Olyan objektumot hoz létre, amellyel frissíthető a hálózati adapterek tulajdonságai a replikált kiszolgálóról.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="8d2bc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8d2bc-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="8d2bc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="8d2bc-105">DESCRIPTION</span></span>
<span data-ttu-id="8d2bc-106">A New-AzMigrateNicMapping parancsmag létrehoz egy leképezést az áttelepíteni kívánt kiszolgálóhoz tartozó forrás NIC-hez.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="8d2bc-107">Ez az objektum bemenetként van megadva a Set-AzMigrateServerReplication parancsmagban a hálózati adapter és a replikált kiszolgálók tulajdonságainak frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="8d2bc-108">Példák</span><span class="sxs-lookup"><span data-stu-id="8d2bc-108">EXAMPLES</span></span>

### <span data-ttu-id="8d2bc-109">1. példa: NIC-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d2bc-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="8d2bc-110">NIC Update objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="8d2bc-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="8d2bc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8d2bc-111">PARAMETERS</span></span>

### <span data-ttu-id="8d2bc-112">-NicI</span><span class="sxs-lookup"><span data-stu-id="8d2bc-112">-NicID</span></span>
<span data-ttu-id="8d2bc-113">A frissítendő NIC AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="8d2bc-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="8d2bc-114">-TargetNicIP</span></span>
<span data-ttu-id="8d2bc-115">A hálózati adapterhez használni kívánt IP-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bc-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="8d2bc-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="8d2bc-117">Azt adja meg, hogy a frissíteni kívánt hálózati adapter az elsődleges, a másodlagos vagy a nincs áttelepítve érték lesz-e.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bc-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="8d2bc-118">-TargetNicSubnet</span></span>
<span data-ttu-id="8d2bc-119">Annak a virtuális hálózati adapternek a hálózati adapterének a neve, amelyhez a kiszolgálót át kell telepíteni.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d2bc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d2bc-120">CommonParameters</span></span>
<span data-ttu-id="8d2bc-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8d2bc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d2bc-122">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8d2bc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d2bc-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2bc-123">INPUTS</span></span>

## <span data-ttu-id="8d2bc-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8d2bc-124">OUTPUTS</span></span>

### <span data-ttu-id="8d2bc-125">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="8d2bc-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="8d2bc-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8d2bc-126">NOTES</span></span>

<span data-ttu-id="8d2bc-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="8d2bc-127">ALIASES</span></span>

## <span data-ttu-id="8d2bc-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8d2bc-128">RELATED LINKS</span></span>

