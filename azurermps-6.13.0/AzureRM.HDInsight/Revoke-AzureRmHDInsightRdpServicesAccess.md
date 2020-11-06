---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 8c3fd2340c1e15d5229a5fdfe9331b1d31c8c02a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503691"
---
# <span data-ttu-id="176e2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="176e2-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="176e2-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="176e2-102">SYNOPSIS</span></span>
<span data-ttu-id="176e2-103">Letiltja a Windows-fürtök RDP-elérését.</span><span class="sxs-lookup"><span data-stu-id="176e2-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="176e2-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="176e2-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="176e2-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="176e2-105">DESCRIPTION</span></span>
<span data-ttu-id="176e2-106">A **Visszavonás-AzureRmHDInsightRdpServicesAccess** parancsmag letiltja a Remote Desktop Protocol (RDP) protokoll elérését egy Windows-alapú Azure HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="176e2-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="176e2-107">Példák</span><span class="sxs-lookup"><span data-stu-id="176e2-107">EXAMPLES</span></span>

### <span data-ttu-id="176e2-108">1. példa: az RDP-hozzáférés letiltása egy adott fürthöz</span><span class="sxs-lookup"><span data-stu-id="176e2-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="176e2-109">Ez a parancs visszavonja az RDP-hozzáférést a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="176e2-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="176e2-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="176e2-110">PARAMETERS</span></span>

### <span data-ttu-id="176e2-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="176e2-111">-ClusterName</span></span>
<span data-ttu-id="176e2-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="176e2-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="176e2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176e2-113">-DefaultProfile</span></span>
<span data-ttu-id="176e2-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="176e2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="176e2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="176e2-115">-ResourceGroupName</span></span>
<span data-ttu-id="176e2-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="176e2-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="176e2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176e2-117">CommonParameters</span></span>
<span data-ttu-id="176e2-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="176e2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176e2-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="176e2-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176e2-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="176e2-120">INPUTS</span></span>

### <span data-ttu-id="176e2-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="176e2-121">None</span></span>

## <span data-ttu-id="176e2-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="176e2-122">OUTPUTS</span></span>

### <span data-ttu-id="176e2-123">System. Void</span><span class="sxs-lookup"><span data-stu-id="176e2-123">System.Void</span></span>

## <span data-ttu-id="176e2-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="176e2-124">NOTES</span></span>

## <span data-ttu-id="176e2-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="176e2-125">RELATED LINKS</span></span>

[<span data-ttu-id="176e2-126">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="176e2-126">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


