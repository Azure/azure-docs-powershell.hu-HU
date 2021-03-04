---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/new-azmigratediskmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/New-AzMigrateDiskMapping.md
ms.openlocfilehash: 1fc58ff016c41e693c059ce792a8dc8aa06e0d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934002"
---
# <span data-ttu-id="93aa2-101">New-AzMigrateDiskMapping</span><span class="sxs-lookup"><span data-stu-id="93aa2-101">New-AzMigrateDiskMapping</span></span>

## <span data-ttu-id="93aa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="93aa2-103">Új lemezleképezés létrehozása</span><span class="sxs-lookup"><span data-stu-id="93aa2-103">Creates a new disk mapping</span></span>

## <span data-ttu-id="93aa2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="93aa2-104">SYNTAX</span></span>

```
New-AzMigrateDiskMapping -DiskID <String> -DiskType <String> -IsOSDisk <String>
 [-DiskEncryptionSetID <String>] [<CommonParameters>]
```

## <span data-ttu-id="93aa2-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="93aa2-105">DESCRIPTION</span></span>
<span data-ttu-id="93aa2-106">A New-AzMigrateDiskMapping parancsmag létrehoz egy megfeleltetést a kiszolgálóhoz csatlakoztatott forráslemezről, amely áttelepíthető</span><span class="sxs-lookup"><span data-stu-id="93aa2-106">The New-AzMigrateDiskMapping cmdlet creates a mapping of the source disk attached to the server to be migrated</span></span>

## <span data-ttu-id="93aa2-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="93aa2-107">EXAMPLES</span></span>

### <span data-ttu-id="93aa2-108">1. példa: Lemezmeghajtók</span><span class="sxs-lookup"><span data-stu-id="93aa2-108">Example 1: Make disks</span></span>
```powershell
PS C:\> New-AzMigrateDiskMapping -DiskID a -DiskType Standard -IsOSDisk 'true'

DiskEncryptionSetId DiskId   DiskType  IsOSDisk LogStorageAccountId LogStorageAccountSasSecretName  
------------------- ------   --------  -------- ------------------- ------------------------------   
                      a      Standard  true  
```

<span data-ttu-id="93aa2-109">Lemezobjektum be- vagy lekérte a New-AzMigrateServerReplication</span><span class="sxs-lookup"><span data-stu-id="93aa2-109">Get disks object to provide input for New-AzMigrateServerReplication</span></span>

## <span data-ttu-id="93aa2-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93aa2-110">PARAMETERS</span></span>

### <span data-ttu-id="93aa2-111">-DiskEncryptionSetID</span><span class="sxs-lookup"><span data-stu-id="93aa2-111">-DiskEncryptionSetID</span></span>
<span data-ttu-id="93aa2-112">A használni használt lemez-encyption-készletet adja meg.</span><span class="sxs-lookup"><span data-stu-id="93aa2-112">Specifies the disk encyption set to be used.</span></span>

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

### <span data-ttu-id="93aa2-113">-DiskID</span><span class="sxs-lookup"><span data-stu-id="93aa2-113">-DiskID</span></span>
<span data-ttu-id="93aa2-114">Annak a lemeznek az azonosítóját adja meg, amely a felderített kiszolgálóhoz van áttelepítve.</span><span class="sxs-lookup"><span data-stu-id="93aa2-114">Specifies the disk ID of the disk attached to the discovered server to be migrated.</span></span>

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

### <span data-ttu-id="93aa2-115">-DiskType</span><span class="sxs-lookup"><span data-stu-id="93aa2-115">-DiskType</span></span>
<span data-ttu-id="93aa2-116">Az Azure VM-hez használt lemeztípust határozza meg.</span><span class="sxs-lookup"><span data-stu-id="93aa2-116">Specifies the type of disks to be used for the Azure VM.</span></span>

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

### <span data-ttu-id="93aa2-117">-IsOSDisk</span><span class="sxs-lookup"><span data-stu-id="93aa2-117">-IsOSDisk</span></span>
<span data-ttu-id="93aa2-118">Azt adja meg, hogy a lemez tartalmazza-e a forráskiszolgáló áttelepíteni kívánt operációs rendszerét.</span><span class="sxs-lookup"><span data-stu-id="93aa2-118">Specifies whether the disk contains the Operating System for the source server to be migrated.</span></span>

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

### <span data-ttu-id="93aa2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93aa2-119">CommonParameters</span></span>
<span data-ttu-id="93aa2-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93aa2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93aa2-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93aa2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93aa2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="93aa2-122">INPUTS</span></span>

## <span data-ttu-id="93aa2-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="93aa2-123">OUTPUTS</span></span>

### <span data-ttu-id="93aa2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span><span class="sxs-lookup"><span data-stu-id="93aa2-124">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IVMwareCbtDiskInput</span></span>

## <span data-ttu-id="93aa2-125">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="93aa2-125">NOTES</span></span>

<span data-ttu-id="93aa2-126">ALIASOK</span><span class="sxs-lookup"><span data-stu-id="93aa2-126">ALIASES</span></span>

## <span data-ttu-id="93aa2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="93aa2-127">RELATED LINKS</span></span>

