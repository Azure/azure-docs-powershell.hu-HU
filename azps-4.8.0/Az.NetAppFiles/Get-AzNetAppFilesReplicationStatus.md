---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/get-aznetappfilesreplicationstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Get-AzNetAppFilesReplicationStatus.md
ms.openlocfilehash: a2345dfe37fd43532739cdfd8000b47fb1e20906
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183464"
---
# <span data-ttu-id="4cba3-101">Get-AzNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="4cba3-101">Get-AzNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="4cba3-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4cba3-102">SYNOPSIS</span></span>
<span data-ttu-id="4cba3-103">A replikáció állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4cba3-103">Get the status of the replication</span></span>

## <span data-ttu-id="4cba3-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4cba3-104">SYNTAX</span></span>

### <span data-ttu-id="4cba3-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4cba3-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cba3-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cba3-106">ByResourceIdParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cba3-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4cba3-107">ByObjectParameterSet</span></span>
```
Get-AzNetAppFilesReplicationStatus -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cba3-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="4cba3-108">DESCRIPTION</span></span>
<span data-ttu-id="4cba3-109">A replikáció állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="4cba3-109">Get the status of the replication</span></span>

## <span data-ttu-id="4cba3-110">Példák</span><span class="sxs-lookup"><span data-stu-id="4cba3-110">EXAMPLES</span></span>

### <span data-ttu-id="4cba3-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="4cba3-111">Example 1</span></span>
```powershell
PS C:\> Get-AnfReplicationStatus -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -PoolName "MyDestinationPool" -VolumeName "MyVol"

Output:

Healthy            : true
RelationshipStatus : Idle
MirrorState        : Mirrored
TotalProgress      : 1024
ErrorMessage       :
```

<span data-ttu-id="4cba3-112">Ez a parancs a MyVol replikációs állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="4cba3-112">This command gets the status of replication on MyVol</span></span>

## <span data-ttu-id="4cba3-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4cba3-113">PARAMETERS</span></span>

### <span data-ttu-id="4cba3-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4cba3-114">-AccountName</span></span>
<span data-ttu-id="4cba3-115">A replikációs célként megadott kötet ANF-fiókjának neve</span><span class="sxs-lookup"><span data-stu-id="4cba3-115">The name of the ANF account of the replication destination volume</span></span>

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

### <span data-ttu-id="4cba3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cba3-116">-DefaultProfile</span></span>
<span data-ttu-id="4cba3-117">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4cba3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cba3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4cba3-118">-InputObject</span></span>
<span data-ttu-id="4cba3-119">A ANF replikációs cél mennyiségi objektuma a replikációs állapot eléréséhez</span><span class="sxs-lookup"><span data-stu-id="4cba3-119">The ANF replication destination volume object to get replication status</span></span>

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

### <span data-ttu-id="4cba3-120">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4cba3-120">-Name</span></span>
<span data-ttu-id="4cba3-121">A ANF replikációs cél kötetének neve</span><span class="sxs-lookup"><span data-stu-id="4cba3-121">The name of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4cba3-122">-PoolName</span><span class="sxs-lookup"><span data-stu-id="4cba3-122">-PoolName</span></span>
<span data-ttu-id="4cba3-123">A replikációs célként megadott kötet ANF-készletének neve</span><span class="sxs-lookup"><span data-stu-id="4cba3-123">The name of the ANF pool of the replication destination volume</span></span>

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

### <span data-ttu-id="4cba3-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cba3-124">-ResourceGroupName</span></span>
<span data-ttu-id="4cba3-125">A ANF replikációs rendeltetési kötetének erőforráscsoport</span><span class="sxs-lookup"><span data-stu-id="4cba3-125">The resource group of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4cba3-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4cba3-126">-ResourceId</span></span>
<span data-ttu-id="4cba3-127">A ANF replikációs célként megadott kötet erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4cba3-127">The resource id of the ANF replication destination volume</span></span>

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

### <span data-ttu-id="4cba3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cba3-128">CommonParameters</span></span>
<span data-ttu-id="4cba3-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4cba3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cba3-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4cba3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cba3-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cba3-131">INPUTS</span></span>

### <span data-ttu-id="4cba3-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4cba3-132">System.String</span></span>

## <span data-ttu-id="4cba3-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4cba3-133">OUTPUTS</span></span>

### <span data-ttu-id="4cba3-134">Microsoft. Azure. Command. NetAppFiles. models. PSNetAppFilesReplicationStatus</span><span class="sxs-lookup"><span data-stu-id="4cba3-134">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationStatus</span></span>

## <span data-ttu-id="4cba3-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4cba3-135">NOTES</span></span>

## <span data-ttu-id="4cba3-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4cba3-136">RELATED LINKS</span></span>
