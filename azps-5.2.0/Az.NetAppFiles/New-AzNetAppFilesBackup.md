---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesBackup.md
ms.openlocfilehash: 66ba63b3e350093173ae9d1badc6c717a3c682aa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359965"
---
# <span data-ttu-id="38361-101">New-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="38361-101">New-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="38361-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38361-102">SYNOPSIS</span></span>
<span data-ttu-id="38361-103">Létrehoz egy új Azure NetApp-fájlokról (ANF) biztonsági másolatot.</span><span class="sxs-lookup"><span data-stu-id="38361-103">Creates a new Azure NetApp Files (ANF) backup.</span></span>

## <span data-ttu-id="38361-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="38361-104">SYNTAX</span></span>

### <span data-ttu-id="38361-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="38361-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesBackup -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> -Label <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38361-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38361-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesBackup -Name <String> -Label <String> -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38361-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="38361-107">DESCRIPTION</span></span>
<span data-ttu-id="38361-108">A **New-AzNetAppFilesBackup** parancsmag biztonsági másolatot készít egy ANF-kötetről.</span><span class="sxs-lookup"><span data-stu-id="38361-108">The **New-AzNetAppFilesBackup** cmdlet creates a backup for an ANF volume.</span></span>

## <span data-ttu-id="38361-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="38361-109">EXAMPLES</span></span>

### <span data-ttu-id="38361-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="38361-110">Example 1</span></span>
```powershell
PS C:\> New-AzNetAppFilesBackup -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyVolumeBackup" -Label "ALabel"
```

<span data-ttu-id="38361-111">Ez a parancs létrehozza az új ANF biztonsági másolatot a "MyVolume" nevű kötethez.</span><span class="sxs-lookup"><span data-stu-id="38361-111">This command creates the new ANF backup for volume named  account "MyVolume".</span></span>

## <span data-ttu-id="38361-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38361-112">PARAMETERS</span></span>

### <span data-ttu-id="38361-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="38361-113">-AccountName</span></span>
<span data-ttu-id="38361-114">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="38361-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="38361-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38361-115">-DefaultProfile</span></span>
<span data-ttu-id="38361-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="38361-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38361-117">-Label</span><span class="sxs-lookup"><span data-stu-id="38361-117">-Label</span></span>
<span data-ttu-id="38361-118">Címke a biztonsági mentéshez</span><span class="sxs-lookup"><span data-stu-id="38361-118">Label for backup</span></span>

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

### <span data-ttu-id="38361-119">-Location</span><span class="sxs-lookup"><span data-stu-id="38361-119">-Location</span></span>
<span data-ttu-id="38361-120">Az erőforrás helye</span><span class="sxs-lookup"><span data-stu-id="38361-120">The location of the resource</span></span>

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

### <span data-ttu-id="38361-121">-Name</span><span class="sxs-lookup"><span data-stu-id="38361-121">-Name</span></span>
<span data-ttu-id="38361-122">Az ANF biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="38361-122">The name of the ANF backup</span></span>

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

### <span data-ttu-id="38361-123">-PoolName</span><span class="sxs-lookup"><span data-stu-id="38361-123">-PoolName</span></span>
<span data-ttu-id="38361-124">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="38361-124">The name of the ANF pool</span></span>

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

### <span data-ttu-id="38361-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38361-125">-ResourceGroupName</span></span>
<span data-ttu-id="38361-126">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="38361-126">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="38361-127">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="38361-127">-VolumeName</span></span>
<span data-ttu-id="38361-128">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="38361-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="38361-129">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="38361-129">-VolumeObject</span></span>
<span data-ttu-id="38361-130">Az új biztonságimásolat-objektum hangereje</span><span class="sxs-lookup"><span data-stu-id="38361-130">The volume for the new backup object</span></span>

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

### <span data-ttu-id="38361-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38361-131">-Confirm</span></span>
<span data-ttu-id="38361-132">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="38361-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38361-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38361-133">-WhatIf</span></span>
<span data-ttu-id="38361-134">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="38361-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38361-135">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="38361-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38361-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38361-136">CommonParameters</span></span>
<span data-ttu-id="38361-137">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38361-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38361-138">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="38361-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38361-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38361-139">INPUTS</span></span>

### <span data-ttu-id="38361-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="38361-140">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="38361-141">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="38361-141">OUTPUTS</span></span>

### <span data-ttu-id="38361-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="38361-142">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="38361-143">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="38361-143">NOTES</span></span>

## <span data-ttu-id="38361-144">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="38361-144">RELATED LINKS</span></span>
