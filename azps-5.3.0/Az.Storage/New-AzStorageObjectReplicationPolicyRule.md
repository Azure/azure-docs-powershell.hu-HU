---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98466924"
---
# <span data-ttu-id="728db-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="728db-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="728db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="728db-102">SYNOPSIS</span></span>
<span data-ttu-id="728db-103">Objektumreplikációs házirendszabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="728db-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="728db-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="728db-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="728db-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="728db-105">DESCRIPTION</span></span>
<span data-ttu-id="728db-106">A **Get-AzStorageObjectReplicationPolicy parancsmag** létrehoz egy objektumreplikációs házirendszabályt, amelyet egy Set-AzStorageObjectReplicationPolicy fog használni.</span><span class="sxs-lookup"><span data-stu-id="728db-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="728db-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="728db-107">EXAMPLES</span></span>

### <span data-ttu-id="728db-108">1. példa: Objektum-replikációs házirendszabály létrehozása csak forrás- és célfiók esetén, és a tulajdonságainak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="728db-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="728db-109">Ez a parancs létrehoz egy olyan objektum-replikációs házirendszabályt, amely csak a forrás- és a célfiókot veszi fel, és annak tulajdonságait is megmutatja.</span><span class="sxs-lookup"><span data-stu-id="728db-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="728db-110">2. példa: Objektum-replikációs házirendszabály létrehozása az összes tulajdonsággal, és a tulajdonságainak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="728db-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="728db-111">Ez a parancs egy objektumreplikációs házirendszabály minden tulajdonsággal és a tulajdonságainak megjelenítése.</span><span class="sxs-lookup"><span data-stu-id="728db-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="728db-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="728db-112">PARAMETERS</span></span>

### <span data-ttu-id="728db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728db-113">-DefaultProfile</span></span>
<span data-ttu-id="728db-114">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="728db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="728db-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="728db-115">-DestinationContainer</span></span>
<span data-ttu-id="728db-116">A céltároló neve, amelybe replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="728db-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="728db-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="728db-117">-MinCreationTime</span></span>
<span data-ttu-id="728db-118">Az idő után létrehozott blobok replikálódnak a célhelyre.</span><span class="sxs-lookup"><span data-stu-id="728db-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728db-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="728db-119">-PrefixMatch</span></span>
<span data-ttu-id="728db-120">Az eredmények szűrésével csak olyan blobokat replikál, amelyeknek a neve a megadott előtaggal kezdődik.</span><span class="sxs-lookup"><span data-stu-id="728db-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="728db-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="728db-121">-RuleId</span></span>
<span data-ttu-id="728db-122">Objektum-replikációs szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="728db-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="728db-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="728db-123">-SourceContainer</span></span>
<span data-ttu-id="728db-124">A forrástároló neve, amelyből replikálni kell.</span><span class="sxs-lookup"><span data-stu-id="728db-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="728db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728db-125">CommonParameters</span></span>
<span data-ttu-id="728db-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="728db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728db-127">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728db-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728db-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="728db-128">INPUTS</span></span>

### <span data-ttu-id="728db-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="728db-129">None</span></span>

## <span data-ttu-id="728db-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="728db-130">OUTPUTS</span></span>

### <span data-ttu-id="728db-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="728db-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="728db-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="728db-132">NOTES</span></span>

## <span data-ttu-id="728db-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="728db-133">RELATED LINKS</span></span>
