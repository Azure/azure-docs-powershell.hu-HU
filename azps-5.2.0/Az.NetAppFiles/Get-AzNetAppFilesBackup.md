---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesbackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesBackup.md
ms.openlocfilehash: 46f6f5d7f9d843a9dd6d30053e9205e52be989d4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360092"
---
# <span data-ttu-id="08e2d-101">Get-AzNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="08e2d-101">Get-AzNetAppFilesBackup</span></span>

## <span data-ttu-id="08e2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="08e2d-103">Részleteket kap az Azure NetApp-fájlokról (ANF) biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="08e2d-103">Gets details of an Azure NetApp Files (ANF) Backup.</span></span>

## <span data-ttu-id="08e2d-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="08e2d-104">SYNTAX</span></span>

### <span data-ttu-id="08e2d-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="08e2d-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesBackup -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 [-VolumeName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08e2d-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08e2d-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="08e2d-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08e2d-107">ByParentObjectParameterSet</span></span>
```
Get-AzNetAppFilesBackup [-Name <String>] -VolumeObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="08e2d-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="08e2d-108">DESCRIPTION</span></span>
<span data-ttu-id="08e2d-109">A **Get-AzNetAppFilesBackup** parancsmag részletes információkat kap az ANF-biztonsági másolatról.</span><span class="sxs-lookup"><span data-stu-id="08e2d-109">The **Get-AzNetAppFilesBackup** cmdlet gets details of an ANF backup.</span></span>

## <span data-ttu-id="08e2d-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="08e2d-110">EXAMPLES</span></span>

### <span data-ttu-id="08e2d-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="08e2d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzNetAppFilesBackup -ResourceGroupName "MyRG" -AccountName "MyAccount" -PoolName "MyPool" -VolumeName "MyVolume" -Name "MyBackup"
```

<span data-ttu-id="08e2d-112">Ez a parancs a MyVolume nevű kötetből a "MyAnfAccount" nevű backcupot kapja.</span><span class="sxs-lookup"><span data-stu-id="08e2d-112">This command gets the backcup named "MyAnfAccount" from the volume named "MyVolume".</span></span>

## <span data-ttu-id="08e2d-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08e2d-113">PARAMETERS</span></span>

### <span data-ttu-id="08e2d-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="08e2d-114">-AccountName</span></span>
<span data-ttu-id="08e2d-115">Az ANF-fiók neve</span><span class="sxs-lookup"><span data-stu-id="08e2d-115">The name of the ANF account</span></span>

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

### <span data-ttu-id="08e2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e2d-116">-DefaultProfile</span></span>
<span data-ttu-id="08e2d-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="08e2d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08e2d-118">-Name</span><span class="sxs-lookup"><span data-stu-id="08e2d-118">-Name</span></span>
<span data-ttu-id="08e2d-119">Az ANF biztonsági másolat neve</span><span class="sxs-lookup"><span data-stu-id="08e2d-119">The name of the ANF backup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e2d-120">-PoolName</span><span class="sxs-lookup"><span data-stu-id="08e2d-120">-PoolName</span></span>
<span data-ttu-id="08e2d-121">Az ANF-készlet neve</span><span class="sxs-lookup"><span data-stu-id="08e2d-121">The name of the ANF pool</span></span>

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

### <span data-ttu-id="08e2d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e2d-122">-ResourceGroupName</span></span>
<span data-ttu-id="08e2d-123">Az ANF-fiók erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="08e2d-123">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="08e2d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08e2d-124">-ResourceId</span></span>
<span data-ttu-id="08e2d-125">Az ANF biztonsági másolat erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="08e2d-125">The resource id of the ANF Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e2d-126">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="08e2d-126">-VolumeName</span></span>
<span data-ttu-id="08e2d-127">Az ANF-kötet neve</span><span class="sxs-lookup"><span data-stu-id="08e2d-127">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e2d-128">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="08e2d-128">-VolumeObject</span></span>
<span data-ttu-id="08e2d-129">A vissza nem térő biztonsági másolatot tartalmazó kötetobjektum</span><span class="sxs-lookup"><span data-stu-id="08e2d-129">The volume object containing the backup to return</span></span>

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

### <span data-ttu-id="08e2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e2d-130">CommonParameters</span></span>
<span data-ttu-id="08e2d-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e2d-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08e2d-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e2d-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="08e2d-133">INPUTS</span></span>

### <span data-ttu-id="08e2d-134">System.String</span><span class="sxs-lookup"><span data-stu-id="08e2d-134">System.String</span></span>

### <span data-ttu-id="08e2d-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="08e2d-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="08e2d-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="08e2d-136">OUTPUTS</span></span>

### <span data-ttu-id="08e2d-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span><span class="sxs-lookup"><span data-stu-id="08e2d-137">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesBackup</span></span>

## <span data-ttu-id="08e2d-138">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="08e2d-138">NOTES</span></span>

## <span data-ttu-id="08e2d-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="08e2d-139">RELATED LINKS</span></span>
