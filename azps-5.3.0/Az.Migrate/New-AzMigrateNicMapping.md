---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratenicmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateNicMapping.md
ms.openlocfilehash: 118e96747d3859a7b9132747052fb3407b7201ae
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385768"
---
# <span data-ttu-id="26856-101">New-AzMigrateNicMapping</span><span class="sxs-lookup"><span data-stu-id="26856-101">New-AzMigrateNicMapping</span></span>

## <span data-ttu-id="26856-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26856-102">SYNOPSIS</span></span>
<span data-ttu-id="26856-103">Egy objektumot hoz létre a replikáló kiszolgáló NIC-tulajdonságainak frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="26856-103">Creates an object to update NIC properties of a replicating server.</span></span>

## <span data-ttu-id="26856-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="26856-104">SYNTAX</span></span>

```
New-AzMigrateNicMapping -NicID <String> [-TargetNicIP <String>] [-TargetNicSelectionType <String>]
 [-TargetNicSubnet <String>] [<CommonParameters>]
```

## <span data-ttu-id="26856-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="26856-105">DESCRIPTION</span></span>
<span data-ttu-id="26856-106">A New-AzMigrateNicMapping parancsmag létrehozza az áttelepíteni megfelelő kiszolgálóhoz csatolt forrás NIC megfeleltetését.</span><span class="sxs-lookup"><span data-stu-id="26856-106">The New-AzMigrateNicMapping cmdlet creates a mapping of the source NIC attached to the server to be migrated.</span></span>
<span data-ttu-id="26856-107">Ez az objektum bemenetként szolgál a Set-AzMigrateServerReplication parancsmagnak a NIC frissítéséhez és egy replikáló kiszolgáló tulajdonságainak frissítéséhez.</span><span class="sxs-lookup"><span data-stu-id="26856-107">This object is provided as an input to the Set-AzMigrateServerReplication cmdlet to update the NIC and its properties for a replicating server.</span></span>

## <span data-ttu-id="26856-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="26856-108">EXAMPLES</span></span>

### <span data-ttu-id="26856-109">1. példa: NIC-objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="26856-109">Example 1: Create a NIC object</span></span>
```powershell
PS C:\> New-AzMigrateNicMapping -NicID a2399354-653a-464e-a567-d30ef5467a31 -TargetNicSelectionType primary -TargetNicIP "172.17.1.17"

IsPrimaryNic IsSelectedForMigration NicId                                TargetStaticIPAddress TargetSubnetName
------------ ---------------------- -----                                --------------------- ----------------
false        false                  a2399354-653a-464e-a567-d30ef5467a31
```

<span data-ttu-id="26856-110">Nic frissítési objektumot hoz létre.</span><span class="sxs-lookup"><span data-stu-id="26856-110">Creates a NIC update object.</span></span>

## <span data-ttu-id="26856-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26856-111">PARAMETERS</span></span>

### <span data-ttu-id="26856-112">-NicID</span><span class="sxs-lookup"><span data-stu-id="26856-112">-NicID</span></span>
<span data-ttu-id="26856-113">A frissítenie kell a NIC azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="26856-113">Specifies the ID of the NIC to be updated.</span></span>

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

### <span data-ttu-id="26856-114">-TargetNicIP</span><span class="sxs-lookup"><span data-stu-id="26856-114">-TargetNicIP</span></span>
<span data-ttu-id="26856-115">A NIC-hez használt cél alhálózat ip-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="26856-115">Specifies the IP within the destination subnet to be used for the NIC.</span></span>

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

### <span data-ttu-id="26856-116">-TargetNicSelectionType</span><span class="sxs-lookup"><span data-stu-id="26856-116">-TargetNicSelectionType</span></span>
<span data-ttu-id="26856-117">Azt adja meg, hogy a frissíthető NIC lesz-e az elsődleges, másodlagos vagy nem migrálható.</span><span class="sxs-lookup"><span data-stu-id="26856-117">Specifies whether the NIC to be updated will be the primary, secondary or not migrated.</span></span>

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

### <span data-ttu-id="26856-118">-TargetNicSubnet</span><span class="sxs-lookup"><span data-stu-id="26856-118">-TargetNicSubnet</span></span>
<span data-ttu-id="26856-119">A NIC alhálózati nevét adja meg abban a cél virtuális hálózatban, amelybe a kiszolgálót át kell migrálni.</span><span class="sxs-lookup"><span data-stu-id="26856-119">Specifies the Subnet name for the NIC in the destination Virtual Network to which the server needs to be migrated.</span></span>

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

### <span data-ttu-id="26856-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26856-120">CommonParameters</span></span>
<span data-ttu-id="26856-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26856-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26856-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26856-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26856-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26856-123">INPUTS</span></span>

## <span data-ttu-id="26856-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="26856-124">OUTPUTS</span></span>

### <span data-ttu-id="26856-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span><span class="sxs-lookup"><span data-stu-id="26856-125">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtNicInput</span></span>

## <span data-ttu-id="26856-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="26856-126">NOTES</span></span>

<span data-ttu-id="26856-127">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="26856-127">ALIASES</span></span>

## <span data-ttu-id="26856-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="26856-128">RELATED LINKS</span></span>

