---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: 73efd000f6889675c3daf9f99821640a8b6fbb99
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926921"
---
# <span data-ttu-id="3f333-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="3f333-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="3f333-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f333-102">SYNOPSIS</span></span>
<span data-ttu-id="3f333-103">A replikáció állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3f333-103">Get the status of the replication</span></span>

## <span data-ttu-id="3f333-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="3f333-104">SYNTAX</span></span>

### <span data-ttu-id="3f333-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="3f333-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3f333-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f333-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3f333-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f333-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3f333-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="3f333-108">DESCRIPTION</span></span>
<span data-ttu-id="3f333-109">A replikáció állapotának ellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3f333-109">Get the status of the replication</span></span>

## <span data-ttu-id="3f333-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="3f333-110">EXAMPLES</span></span>

### <span data-ttu-id="3f333-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="3f333-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="3f333-112">Ez a parancs a replikáció állapotát kapja meg a MyVolen</span><span class="sxs-lookup"><span data-stu-id="3f333-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="3f333-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f333-113">PARAMETERS</span></span>

### <span data-ttu-id="3f333-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3f333-114">-AccountName</span></span>
<span data-ttu-id="3f333-115">A replikációs célkötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="3f333-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="3f333-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f333-116">-DefaultProfile</span></span>
<span data-ttu-id="3f333-117">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="3f333-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f333-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f333-118">-InputObject</span></span>
<span data-ttu-id="3f333-119">AnF replikációs célhelyének kötetobjektuma a replikáció állapotának leellenőrzése</span><span class="sxs-lookup"><span data-stu-id="3f333-119">The ANF replication destination volume object to get replication status</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f333-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f333-120">-Name</span></span>
<span data-ttu-id="3f333-121">Az ANF-replikációs célkötet neve</span><span class="sxs-lookup"><span data-stu-id="3f333-121">The name of the ANF replication destination volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f333-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="3f333-122">-PoolName</span></span>
<span data-ttu-id="3f333-123">A replikációs célkötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="3f333-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="3f333-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f333-124">-ResourceGroupName</span></span>
<span data-ttu-id="3f333-125">Az ANF-replikációs célkötet erőforráscsoportja</span><span class="sxs-lookup"><span data-stu-id="3f333-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="3f333-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f333-126">-ResourceId</span></span>
<span data-ttu-id="3f333-127">Az ANF-replikációs célkötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="3f333-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="3f333-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f333-128">CommonParameters</span></span>
<span data-ttu-id="3f333-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f333-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f333-130">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f333-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f333-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3f333-131">INPUTS</span></span>

### <span data-ttu-id="3f333-132">System.String</span><span class="sxs-lookup"><span data-stu-id="3f333-132">System.String</span></span>

### <span data-ttu-id="3f333-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="3f333-133">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="3f333-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="3f333-134">OUTPUTS</span></span>

### <span data-ttu-id="3f333-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="3f333-135">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="3f333-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="3f333-136">NOTES</span></span>

## <span data-ttu-id="3f333-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="3f333-137">RELATED LINKS</span></span>
