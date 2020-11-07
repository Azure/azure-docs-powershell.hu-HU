---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666361"
---
# <span data-ttu-id="564c4-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="564c4-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="564c4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="564c4-102">SYNOPSIS</span></span>
<span data-ttu-id="564c4-103">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="564c4-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="564c4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="564c4-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="564c4-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="564c4-105">DESCRIPTION</span></span>
<span data-ttu-id="564c4-106">A **Grant-AzHDInsightRdpServicesAccess** parancsmag lehetővé teszi a Remote Desktop Protocol (RDP) protokollnak a Windows-alapú Azure HDInsight-fürtök elérését.</span><span class="sxs-lookup"><span data-stu-id="564c4-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="564c4-107">Példák</span><span class="sxs-lookup"><span data-stu-id="564c4-107">EXAMPLES</span></span>

### <span data-ttu-id="564c4-108">1. példa: az Azure HDInsight-fürtök RDP-elérésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="564c4-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="564c4-109">Ez a parancs RDP-hozzáférést ad a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="564c4-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="564c4-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="564c4-110">PARAMETERS</span></span>

### <span data-ttu-id="564c4-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="564c4-111">-ClusterName</span></span>
<span data-ttu-id="564c4-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="564c4-112">Specifies the name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="564c4-113">-DefaultProfile</span></span>
<span data-ttu-id="564c4-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="564c4-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="564c4-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="564c4-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="564c4-116">A fürt RDP-eléréséhez használt **datetime** objektumként adja meg a lejárat időpontját.</span><span class="sxs-lookup"><span data-stu-id="564c4-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564c4-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="564c4-117">-RdpCredential</span></span>
<span data-ttu-id="564c4-118">A fürt RDP-hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="564c4-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="564c4-119">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="564c4-119">This is only for Windows clusters.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="564c4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="564c4-120">-ResourceGroupName</span></span>
<span data-ttu-id="564c4-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="564c4-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="564c4-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="564c4-122">CommonParameters</span></span>
<span data-ttu-id="564c4-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="564c4-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="564c4-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="564c4-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="564c4-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="564c4-125">INPUTS</span></span>

### <span data-ttu-id="564c4-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="564c4-126">None</span></span>

## <span data-ttu-id="564c4-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="564c4-127">OUTPUTS</span></span>

### <span data-ttu-id="564c4-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="564c4-128">System.Void</span></span>

## <span data-ttu-id="564c4-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="564c4-129">NOTES</span></span>

## <span data-ttu-id="564c4-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="564c4-130">RELATED LINKS</span></span>

[<span data-ttu-id="564c4-131">Visszavonás-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="564c4-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


