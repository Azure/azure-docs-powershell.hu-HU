---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 812b1a3de090240a306f3d0a5b768ce25f3b22e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203604"
---
# <span data-ttu-id="0c931-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="0c931-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="0c931-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c931-102">SYNOPSIS</span></span>
<span data-ttu-id="0c931-103">Új lemezleképezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="0c931-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="0c931-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0c931-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <DiskAccountType> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="0c931-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0c931-105">DESCRIPTION</span></span>
<span data-ttu-id="0c931-106">A New-AzMigrateDiskMapping parancsmag létrehoz egy megfeleltetést a kiszolgálóhoz csatlakoztatott forráslemezről, amely áttelepíthető</span><span class="sxs-lookup"><span data-stu-id="0c931-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="0c931-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0c931-107">EXAMPLES</span></span>

### <span data-ttu-id="0c931-108">1. példa: Lemezeket</span><span class="sxs-lookup"><span data-stu-id="0c931-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="0c931-109">Lemezobjektum be- és bevitelének New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="0c931-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="0c931-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c931-110">PARAMETERS</span></span>

### <span data-ttu-id="0c931-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="0c931-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="0c931-112">A használni használt lemez-encyption-készletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="0c931-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="0c931-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="0c931-113">-DiskID</span></span>
<span data-ttu-id="0c931-114">Annak a lemeznek az azonosítóját adja meg, amely a felderített kiszolgálóhoz van csatlakoztatva, és amely áttelepíthető.</span><span class="sxs-lookup"><span data-stu-id="0c931-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="0c931-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="0c931-115">-DiskType</span></span>
<span data-ttu-id="0c931-116">Az Azure VM-hez használt lemeztípust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="0c931-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="0c931-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="0c931-117">-IsOSDisk</span></span>
<span data-ttu-id="0c931-118">Azt adja meg, hogy a lemez tartalmazza-e a forráskiszolgáló áttelepíteni kívánt operációs rendszerét.</span><span class="sxs-lookup"><span data-stu-id="0c931-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="0c931-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c931-119">CommonParameters</span></span>
<span data-ttu-id="0c931-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c931-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c931-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c931-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c931-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c931-122">INPUTS</span></span>

## <span data-ttu-id="0c931-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0c931-123">OUTPUTS</span></span>

### <span data-ttu-id="0c931-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="0c931-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="0c931-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0c931-125">NOTES</span></span>

<span data-ttu-id="0c931-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="0c931-126">ALIASES</span></span>

## <span data-ttu-id="0c931-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0c931-127">RELATED LINKS</span></span>

