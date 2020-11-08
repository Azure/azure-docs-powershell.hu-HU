---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94194579"
---
# <span data-ttu-id="9e48c-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="9e48c-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="9e48c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9e48c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e48c-103">Új lemez-hozzárendelés létrehozása</span><span class="sxs-lookup"><span data-stu-id="9e48c-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="9e48c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9e48c-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="9e48c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9e48c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e48c-106">A New-AzMigrateDiskMapping parancsmag létrehoz egy megfeleltetést az áttelepíteni kívánt kiszolgálóhoz a forráshoz.</span><span class="sxs-lookup"><span data-stu-id="9e48c-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="9e48c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9e48c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e48c-108">Példa 1: lemezek készítése</span><span class="sxs-lookup"><span data-stu-id="9e48c-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="9e48c-109">A lemezek objektum beszerzése New-AzMigrateServerReplication beviteléhez</span><span class="sxs-lookup"><span data-stu-id="9e48c-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="9e48c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9e48c-110">PARAMETERS</span></span>

### <span data-ttu-id="9e48c-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="9e48c-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="9e48c-112">Adja meg a használni kívánt encyption.</span><span class="sxs-lookup"><span data-stu-id="9e48c-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="9e48c-113">-Csúszásgátló</span><span class="sxs-lookup"><span data-stu-id="9e48c-113">-DiskID</span></span>
<span data-ttu-id="9e48c-114">Itt adhatja meg, hogy a rendszer milyen lemezmeghajtót szeretne áttelepíteni a felismert kiszolgálóhoz.</span><span class="sxs-lookup"><span data-stu-id="9e48c-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="9e48c-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="9e48c-115">-DiskType</span></span>
<span data-ttu-id="9e48c-116">Az Azure VM-hez használni kívánt lemezek típusát adja meg.</span><span class="sxs-lookup"><span data-stu-id="9e48c-116">Specifies the type of disks to be used for the Azure VM.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Migrate.Support.DiskAccountType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9e48c-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="9e48c-117">-IsOSDisk</span></span>
<span data-ttu-id="9e48c-118">Meghatározza, hogy a lemez tartalmazza-e az áttelepítendő forráskiszolgáló operációs rendszerét.</span><span class="sxs-lookup"><span data-stu-id="9e48c-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="9e48c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e48c-119">CommonParameters</span></span>
<span data-ttu-id="9e48c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9e48c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e48c-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9e48c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e48c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e48c-122">INPUTS</span></span>

## <span data-ttu-id="9e48c-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9e48c-123">OUTPUTS</span></span>

### <span data-ttu-id="9e48c-124">Microsoft. Azure. PowerShell. parancsmagok. áttelepítés. models. Api20180110. IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="9e48c-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="9e48c-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9e48c-125">NOTES</span></span>

<span data-ttu-id="9e48c-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="9e48c-126">ALIASES</span></span>

## <span data-ttu-id="9e48c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9e48c-127">RELATED LINKS</span></span>

