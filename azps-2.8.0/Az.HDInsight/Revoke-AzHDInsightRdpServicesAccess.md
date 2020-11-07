---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666332"
---
# <span data-ttu-id="e528f-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e528f-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="e528f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="e528f-102">SYNOPSIS</span></span>
<span data-ttu-id="e528f-103">Letiltja a Windows-fürtök RDP-elérését.</span><span class="sxs-lookup"><span data-stu-id="e528f-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="e528f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="e528f-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e528f-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="e528f-105">DESCRIPTION</span></span>
<span data-ttu-id="e528f-106">A **Visszavonás-AzHDInsightRdpServicesAccess** parancsmag letiltja a Remote Desktop Protocol (RDP) protokoll elérését egy Windows-alapú Azure HDInsight-fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e528f-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="e528f-107">Példák</span><span class="sxs-lookup"><span data-stu-id="e528f-107">EXAMPLES</span></span>

### <span data-ttu-id="e528f-108">1. példa: az RDP-hozzáférés letiltása egy adott fürthöz</span><span class="sxs-lookup"><span data-stu-id="e528f-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="e528f-109">Ez a parancs visszavonja az RDP-hozzáférést a-Hadoop-001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="e528f-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="e528f-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="e528f-110">PARAMETERS</span></span>

### <span data-ttu-id="e528f-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="e528f-111">-ClusterName</span></span>
<span data-ttu-id="e528f-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e528f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="e528f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e528f-113">-DefaultProfile</span></span>
<span data-ttu-id="e528f-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="e528f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e528f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e528f-115">-ResourceGroupName</span></span>
<span data-ttu-id="e528f-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="e528f-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="e528f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e528f-117">CommonParameters</span></span>
<span data-ttu-id="e528f-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="e528f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e528f-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e528f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e528f-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="e528f-120">INPUTS</span></span>

### <span data-ttu-id="e528f-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="e528f-121">None</span></span>

## <span data-ttu-id="e528f-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="e528f-122">OUTPUTS</span></span>

### <span data-ttu-id="e528f-123">System. Void</span><span class="sxs-lookup"><span data-stu-id="e528f-123">System.Void</span></span>

## <span data-ttu-id="e528f-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="e528f-124">NOTES</span></span>

## <span data-ttu-id="e528f-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="e528f-125">RELATED LINKS</span></span>

[<span data-ttu-id="e528f-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="e528f-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


