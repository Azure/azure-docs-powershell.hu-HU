---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152082"
---
# <span data-ttu-id="0425a-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="0425a-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="0425a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0425a-102">SYNOPSIS</span></span>
<span data-ttu-id="0425a-103">Létrehoz egy új Azure NetApp-fájlokról (ANF) biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="0425a-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="0425a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="0425a-104">SYNTAX</span></span>

### <span data-ttu-id="0425a-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="0425a-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0425a-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0425a-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0425a-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="0425a-107">DESCRIPTION</span></span>
<span data-ttu-id="0425a-108">A **New-AzNetAppFilesBackup** parancsmag biztonsági másolatot készít egy ANF-kötetről.</span><span class="sxs-lookup"><span data-stu-id="0425a-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="0425a-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="0425a-109">EXAMPLES</span></span>

### <span data-ttu-id="0425a-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="0425a-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="0425a-111">Ez a parancs létrehozza az új ANF biztonsági másolatot a "MyVolume" nevű kötethez.</span><span class="sxs-lookup"><span data-stu-id="0425a-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="0425a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0425a-112">PARAMETERS</span></span>

### <span data-ttu-id="0425a-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="0425a-113">-AccountName</span></span>
<span data-ttu-id="0425a-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="0425a-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0425a-115">-DefaultProfile</span></span>
<span data-ttu-id="0425a-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0425a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0425a-117">-Label</span><span class="sxs-lookup"><span data-stu-id="0425a-117">-Label</span></span>
<span data-ttu-id="0425a-118">Címke a biztonsági mentéshez</span><span class="sxs-lookup"><span data-stu-id="0425a-118">Label for backup</span></span>

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

### <span data-ttu-id="0425a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="0425a-119">-Location</span></span>
<span data-ttu-id="0425a-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="0425a-120">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="0425a-121">-Name</span></span>
<span data-ttu-id="0425a-122">Az ANF biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="0425a-122">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="0425a-123">-PoolName</span></span>
<span data-ttu-id="0425a-124">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="0425a-124">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0425a-125">-ResourceGroupName</span></span>
<span data-ttu-id="0425a-126">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="0425a-126">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="0425a-127">-VolumeName</span></span>
<span data-ttu-id="0425a-128">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="0425a-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="0425a-129">-VolumeObject</span></span>
<span data-ttu-id="0425a-130">Az új biztonságimásolat-objektum hangereje</span><span class="sxs-lookup"><span data-stu-id="0425a-130">The volume for the new backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0425a-131">-Confirm</span></span>
<span data-ttu-id="0425a-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="0425a-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0425a-133">-WhatIf</span></span>
<span data-ttu-id="0425a-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="0425a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0425a-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="0425a-135">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0425a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0425a-136">CommonParameters</span></span>
<span data-ttu-id="0425a-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0425a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0425a-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0425a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0425a-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0425a-139">INPUTS</span></span>

### <span data-ttu-id="0425a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="0425a-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="0425a-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0425a-141">OUTPUTS</span></span>

### <span data-ttu-id="0425a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="0425a-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="0425a-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="0425a-143">NOTES</span></span>

## <span data-ttu-id="0425a-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0425a-144">RELATED LINKS</span></span>
