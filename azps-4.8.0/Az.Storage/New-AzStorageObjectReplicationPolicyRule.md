---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182071"
---
# <span data-ttu-id="cfc5c-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cfc5c-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="cfc5c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cfc5c-102">SYNOPSIS</span></span>
<span data-ttu-id="cfc5c-103">Objektum-replikációs házirend-szabályt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="cfc5c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cfc5c-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfc5c-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="cfc5c-105">DESCRIPTION</span></span>
<span data-ttu-id="cfc5c-106">A **Get-AzStorageObjectReplicationPolicy** parancsmag létrehoz egy objektum-replikációs házirend-szabályt, amelyet az Set-AzStorageObjectReplicationPolicy parancsmagban fog használni.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="cfc5c-107">Példák</span><span class="sxs-lookup"><span data-stu-id="cfc5c-107">EXAMPLES</span></span>

### <span data-ttu-id="cfc5c-108">Példa 1: az objektum-replikációs házirend-szabály létrehozása csak a forrás-és a célvárólista segítségével, valamint a tulajdonságaik megjelenítése</span><span class="sxs-lookup"><span data-stu-id="cfc5c-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="cfc5c-109">Ez a parancs létrehoz egy objektum-replikációs házirend-szabályt, amely csak a forrás-és a célországot, valamint a tulajdonságait jeleníti meg.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="cfc5c-110">2. példa: objektum-replikációs házirend-szabály létrehozása az összes tulajdonsággal, és a tulajdonságaik megjelenítése</span><span class="sxs-lookup"><span data-stu-id="cfc5c-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="cfc5c-111">Ez a parancs az objektum replikációs házirend-szabályát az összes tulajdonsággal együtt jeleníti meg, és megjeleníti a tulajdonságait.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="cfc5c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cfc5c-112">PARAMETERS</span></span>

### <span data-ttu-id="cfc5c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfc5c-113">-DefaultProfile</span></span>
<span data-ttu-id="cfc5c-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfc5c-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="cfc5c-115">-DestinationContainer</span></span>
<span data-ttu-id="cfc5c-116">A rendeltetési hely tárolójának neve a replikáláshoz.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="cfc5c-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="cfc5c-117">-MinCreationTime</span></span>
<span data-ttu-id="cfc5c-118">A program az időpont után létrehozott blobokat a célhelyre replikálja..</span><span class="sxs-lookup"><span data-stu-id="cfc5c-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="cfc5c-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="cfc5c-119">-PrefixMatch</span></span>
<span data-ttu-id="cfc5c-120">Szűri az eredményeket úgy, hogy csak azokat a blobokat replikálja, amelyek nevei a megadott előtaggal kezdődnek.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="cfc5c-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="cfc5c-121">-RuleId</span></span>
<span data-ttu-id="cfc5c-122">Az objektum-replikációs szabály azonosítója.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="cfc5c-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="cfc5c-123">-SourceContainer</span></span>
<span data-ttu-id="cfc5c-124">A forrás tároló neve a replikáláshoz.</span><span class="sxs-lookup"><span data-stu-id="cfc5c-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="cfc5c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfc5c-125">CommonParameters</span></span>
<span data-ttu-id="cfc5c-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cfc5c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfc5c-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfc5c-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfc5c-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfc5c-128">INPUTS</span></span>

### <span data-ttu-id="cfc5c-129">Nincs</span><span class="sxs-lookup"><span data-stu-id="cfc5c-129">None</span></span>

## <span data-ttu-id="cfc5c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cfc5c-130">OUTPUTS</span></span>

### <span data-ttu-id="cfc5c-131">Microsoft. Azure. Command. Management. Storage. models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="cfc5c-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="cfc5c-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cfc5c-132">NOTES</span></span>

## <span data-ttu-id="cfc5c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cfc5c-133">RELATED LINKS</span></span>
