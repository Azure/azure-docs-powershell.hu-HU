---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93835981"
---
# <span data-ttu-id="a5458-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5458-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="a5458-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a5458-102">SYNOPSIS</span></span>
<span data-ttu-id="a5458-103">Letiltja a fürt HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="a5458-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="a5458-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a5458-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5458-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="a5458-105">DESCRIPTION</span></span>
<span data-ttu-id="a5458-106">A **Visszavonás-AzHDInsightHttpServicesAccess** parancsmag letiltja a http-hozzáférést az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és az webHCatalog Web Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="a5458-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="a5458-107">Példák</span><span class="sxs-lookup"><span data-stu-id="a5458-107">EXAMPLES</span></span>

### <span data-ttu-id="a5458-108">Példa 1: a fürt HTTP-elérésének letiltása</span><span class="sxs-lookup"><span data-stu-id="a5458-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="a5458-109">Ez a parancs visszavonja a HTTP-hozzáférést a-hadoop_001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="a5458-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="a5458-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a5458-110">PARAMETERS</span></span>

### <span data-ttu-id="a5458-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="a5458-111">-ClusterName</span></span>
<span data-ttu-id="a5458-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5458-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="a5458-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5458-113">-DefaultProfile</span></span>
<span data-ttu-id="a5458-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="a5458-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5458-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5458-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5458-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="a5458-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="a5458-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5458-117">CommonParameters</span></span>
<span data-ttu-id="a5458-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a5458-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5458-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5458-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5458-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5458-120">INPUTS</span></span>

### <span data-ttu-id="a5458-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="a5458-121">None</span></span>

## <span data-ttu-id="a5458-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a5458-122">OUTPUTS</span></span>

### <span data-ttu-id="a5458-123">Microsoft. Azure. Management. HDInsight. models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="a5458-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="a5458-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a5458-124">NOTES</span></span>

## <span data-ttu-id="a5458-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a5458-125">RELATED LINKS</span></span>

[<span data-ttu-id="a5458-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a5458-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


