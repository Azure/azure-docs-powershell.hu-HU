---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/grant-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: ce169dc1cce1552b48aa864885c6877624da0176
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495118"
---
# <span data-ttu-id="fe1f5-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe1f5-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="fe1f5-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fe1f5-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1f5-103">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe1f5-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fe1f5-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe1f5-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fe1f5-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1f5-106">A **Grant-AzureRmHDInsightRdpServicesAccess** parancsmag lehetővé teszi a Remote Desktop Protocol (RDP) protokollnak a Windows-alapú Azure HDInsight-fürtök elérését.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fe1f5-107">Példák</span><span class="sxs-lookup"><span data-stu-id="fe1f5-107">EXAMPLES</span></span>

### <span data-ttu-id="fe1f5-108">1. példa: az Azure HDInsight-fürtök RDP-elérésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="fe1f5-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="fe1f5-109">Ez a parancs RDP-hozzáférést ad a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="fe1f5-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fe1f5-110">PARAMETERS</span></span>

### <span data-ttu-id="fe1f5-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="fe1f5-111">-ClusterName</span></span>
<span data-ttu-id="fe1f5-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="fe1f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1f5-113">-DefaultProfile</span></span>
<span data-ttu-id="fe1f5-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="fe1f5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f5-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="fe1f5-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="fe1f5-116">A fürt RDP-eléréséhez használt **datetime** objektumként adja meg a lejárat időpontját.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="fe1f5-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="fe1f5-117">-RdpCredential</span></span>
<span data-ttu-id="fe1f5-118">A fürt RDP-hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="fe1f5-119">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="fe1f5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1f5-120">-ResourceGroupName</span></span>
<span data-ttu-id="fe1f5-121">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="fe1f5-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="fe1f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1f5-122">CommonParameters</span></span>
<span data-ttu-id="fe1f5-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fe1f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1f5-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe1f5-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1f5-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe1f5-125">INPUTS</span></span>

### <span data-ttu-id="fe1f5-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="fe1f5-126">None</span></span>

## <span data-ttu-id="fe1f5-127">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fe1f5-127">OUTPUTS</span></span>

### <span data-ttu-id="fe1f5-128">System. Void</span><span class="sxs-lookup"><span data-stu-id="fe1f5-128">System.Void</span></span>

## <span data-ttu-id="fe1f5-129">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fe1f5-129">NOTES</span></span>

## <span data-ttu-id="fe1f5-130">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fe1f5-130">RELATED LINKS</span></span>

[<span data-ttu-id="fe1f5-131">Visszavonás-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="fe1f5-131">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


