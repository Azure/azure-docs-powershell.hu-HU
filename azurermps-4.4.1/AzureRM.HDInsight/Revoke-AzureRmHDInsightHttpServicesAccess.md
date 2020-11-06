---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 795882aa421037252ca920093f1df39b4e242fce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93493503"
---
# <span data-ttu-id="40ab8-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="40ab8-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="40ab8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40ab8-102">SYNOPSIS</span></span>
<span data-ttu-id="40ab8-103">Letiltja a fürt HTTP-elérését.</span><span class="sxs-lookup"><span data-stu-id="40ab8-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40ab8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40ab8-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40ab8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40ab8-105">DESCRIPTION</span></span>
<span data-ttu-id="40ab8-106">A **Visszavonás-AzureRmHDInsightHttpServicesAccess** parancsmag letiltja a http-hozzáférést az Azure HDInsight-fürtökhöz az ODBC, a Ambari, a Oozie és az webHCatalog Web Services szolgáltatáshoz.</span><span class="sxs-lookup"><span data-stu-id="40ab8-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="40ab8-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40ab8-107">EXAMPLES</span></span>

### <span data-ttu-id="40ab8-108">Példa 1: a fürt HTTP-elérésének letiltása</span><span class="sxs-lookup"><span data-stu-id="40ab8-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="40ab8-109">Ez a parancs visszavonja a HTTP-hozzáférést a-hadoop_001 nevű fürthöz.</span><span class="sxs-lookup"><span data-stu-id="40ab8-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="40ab8-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40ab8-110">PARAMETERS</span></span>

### <span data-ttu-id="40ab8-111">-Fürtnév</span><span class="sxs-lookup"><span data-stu-id="40ab8-111">-ClusterName</span></span>
<span data-ttu-id="40ab8-112">A fürt nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40ab8-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="40ab8-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40ab8-113">-ResourceGroupName</span></span>
<span data-ttu-id="40ab8-114">Az erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="40ab8-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="40ab8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40ab8-115">-DefaultProfile</span></span>
<span data-ttu-id="40ab8-116">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40ab8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40ab8-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40ab8-117">CommonParameters</span></span>
<span data-ttu-id="40ab8-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40ab8-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40ab8-119">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40ab8-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40ab8-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40ab8-120">INPUTS</span></span>

## <span data-ttu-id="40ab8-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40ab8-121">OUTPUTS</span></span>

### <span data-ttu-id="40ab8-122">Microsoft. Azure. Management. HDInsight. models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="40ab8-122">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="40ab8-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40ab8-123">NOTES</span></span>

## <span data-ttu-id="40ab8-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40ab8-124">RELATED LINKS</span></span>

[<span data-ttu-id="40ab8-125">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="40ab8-125">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


