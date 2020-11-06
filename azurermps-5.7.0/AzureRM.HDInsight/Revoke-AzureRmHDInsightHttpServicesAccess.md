---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 388e339ba7545bc2e4d00166a6f365a19cb44f28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499844"
---
# <span data-ttu-id="bf0bf-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf0bf-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="bf0bf-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bf0bf-102">SYNOPSIS</span></span>
<span data-ttu-id="bf0bf-103">Letiltja a fürt HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf0bf-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bf0bf-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf0bf-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="bf0bf-105">DESCRIPTION</span></span>
<span data-ttu-id="bf0bf-106">A **Visszavonás-AzureRmHDInsightHttpServicesAccess** parancsmag letiltja a http-hozzáférést az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és az webHCatalog Web Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="bf0bf-107">Példák</span><span class="sxs-lookup"><span data-stu-id="bf0bf-107">EXAMPLES</span></span>

### <span data-ttu-id="bf0bf-108">Példa 1: a fürt HTTP-elérésének letiltása</span><span class="sxs-lookup"><span data-stu-id="bf0bf-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="bf0bf-109">Ez a parancs visszavonja a HTTP-hozzáférést a-hadoop_001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="bf0bf-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bf0bf-110">PARAMETERS</span></span>

### <span data-ttu-id="bf0bf-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="bf0bf-111">-ClusterName</span></span>
<span data-ttu-id="bf0bf-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf0bf-113">-DefaultProfile</span></span>
<span data-ttu-id="bf0bf-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="bf0bf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0bf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf0bf-115">-ResourceGroupName</span></span>
<span data-ttu-id="bf0bf-116">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf0bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf0bf-117">CommonParameters</span></span>
<span data-ttu-id="bf0bf-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bf0bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf0bf-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf0bf-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf0bf-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf0bf-120">INPUTS</span></span>

### <span data-ttu-id="bf0bf-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="bf0bf-121">None</span></span>
<span data-ttu-id="bf0bf-122">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="bf0bf-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf0bf-123">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bf0bf-123">OUTPUTS</span></span>

### <span data-ttu-id="bf0bf-124">Microsoft. Azure. Management. HDInsight. models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="bf0bf-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="bf0bf-125">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bf0bf-125">NOTES</span></span>

## <span data-ttu-id="bf0bf-126">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bf0bf-126">RELATED LINKS</span></span>

[<span data-ttu-id="bf0bf-127">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="bf0bf-127">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


