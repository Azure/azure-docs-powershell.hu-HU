---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 22d2f4617e5b8a268de8518695d5217191a211df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504987"
---
# <span data-ttu-id="b8c6d-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b8c6d-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="b8c6d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b8c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8c6d-103">RDP-elérést ad vissza a Windows-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8c6d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b8c6d-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8c6d-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b8c6d-105">DESCRIPTION</span></span>
<span data-ttu-id="b8c6d-106">A **Grant-AzureRmHDInsightRdpServicesAccess** parancsmag lehetővé teszi a Remote Desktop Protocol (RDP) protokollnak a Windows-alapú Azure HDInsight-fürtök elérését.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="b8c6d-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b8c6d-107">EXAMPLES</span></span>

### <span data-ttu-id="b8c6d-108">1. példa: az Azure HDInsight-fürtök RDP-elérésének engedélyezése</span><span class="sxs-lookup"><span data-stu-id="b8c6d-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="b8c6d-109">Ez a parancs RDP-hozzáférést ad a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="b8c6d-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b8c6d-110">PARAMETERS</span></span>

### <span data-ttu-id="b8c6d-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="b8c6d-111">-ClusterName</span></span>
<span data-ttu-id="b8c6d-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="b8c6d-113">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="b8c6d-113">-RdpAccessExpiry</span></span>
<span data-ttu-id="b8c6d-114">A fürt RDP-eléréséhez használt **datetime** objektumként adja meg a lejárat időpontját.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-114">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="b8c6d-115">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="b8c6d-115">-RdpCredential</span></span>
<span data-ttu-id="b8c6d-116">A fürt RDP-hitelesítő adatait adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-116">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="b8c6d-117">Ez csak Windows-fürtök esetén használható.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-117">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="b8c6d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8c6d-118">-ResourceGroupName</span></span>
<span data-ttu-id="b8c6d-119">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="b8c6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8c6d-120">-DefaultProfile</span></span>
<span data-ttu-id="b8c6d-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b8c6d-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8c6d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8c6d-122">CommonParameters</span></span>
<span data-ttu-id="b8c6d-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b8c6d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8c6d-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8c6d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8c6d-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c6d-125">INPUTS</span></span>

## <span data-ttu-id="b8c6d-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b8c6d-126">OUTPUTS</span></span>

### <span data-ttu-id="b8c6d-127">System. Void</span><span class="sxs-lookup"><span data-stu-id="b8c6d-127">System.Void</span></span>

## <span data-ttu-id="b8c6d-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b8c6d-128">NOTES</span></span>

## <span data-ttu-id="b8c6d-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b8c6d-129">RELATED LINKS</span></span>

[<span data-ttu-id="b8c6d-130">Visszavonás-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="b8c6d-130">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


