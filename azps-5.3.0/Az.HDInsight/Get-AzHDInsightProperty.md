---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: e13b90da8e1901faf0b18eb6ebf3cc78ce1bbcda
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469673"
---
# <span data-ttu-id="2fa53-101">Get-AzHDInsightProperty</span><span class="sxs-lookup"><span data-stu-id="2fa53-101">Get-AzHDInsightProperty</span></span>

## <span data-ttu-id="2fa53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa53-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa53-103">Beszerzheti a HDInsight szolgáltatás tulajdonságait, például az elérhető helyeket és a kapacitást.</span><span class="sxs-lookup"><span data-stu-id="2fa53-103">Gets properties about the HDInsight service, such as available locations and capacity.</span></span>

## <span data-ttu-id="2fa53-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2fa53-104">SYNTAX</span></span>

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fa53-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2fa53-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa53-106">A **Get-AzHDInsightProperty** parancsmag az Azure HDInsight-re jellemző tulajdonságokat kap, például az elérhető helyek listáját, a HDInsight-fürtverziókat és az elérhető számítási kapacitást.</span><span class="sxs-lookup"><span data-stu-id="2fa53-106">The **Get-AzHDInsightProperty** cmdlet gets properties specific to Azure HDInsight, such as the list of available locations, HDInsight cluster versions, and available compute capacity.</span></span>

## <span data-ttu-id="2fa53-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2fa53-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa53-108">1. példa: Azure HDInsight-fürt tulajdonságainak lekérte</span><span class="sxs-lookup"><span data-stu-id="2fa53-108">Example 1: Get the properties of an Azure HDInsight cluster</span></span>
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

<span data-ttu-id="2fa53-109">Ez a parancs hdinsight-szolgáltatásból kap tulajdonságokat az US 2.2-től keletre.</span><span class="sxs-lookup"><span data-stu-id="2fa53-109">This command gets properties from an HDInsight service from location East US 2.</span></span>

## <span data-ttu-id="2fa53-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fa53-110">PARAMETERS</span></span>

### <span data-ttu-id="2fa53-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fa53-111">-DefaultProfile</span></span>
<span data-ttu-id="2fa53-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2fa53-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fa53-113">-Location</span><span class="sxs-lookup"><span data-stu-id="2fa53-113">-Location</span></span>
<span data-ttu-id="2fa53-114">Azt a helyet adja meg, ahol lekéri a HDInsight-tulajdonságokat.</span><span class="sxs-lookup"><span data-stu-id="2fa53-114">Specifies the location for which to fetch HDInsight properties.</span></span>

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

### <span data-ttu-id="2fa53-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa53-115">CommonParameters</span></span>
<span data-ttu-id="2fa53-116">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fa53-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa53-117">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2fa53-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa53-118">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2fa53-118">INPUTS</span></span>

### <span data-ttu-id="2fa53-119">Nincs</span><span class="sxs-lookup"><span data-stu-id="2fa53-119">None</span></span>
## <span data-ttu-id="2fa53-120">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2fa53-120">OUTPUTS</span></span>

### <span data-ttu-id="2fa53-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span><span class="sxs-lookup"><span data-stu-id="2fa53-121">Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities</span></span>
## <span data-ttu-id="2fa53-122">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2fa53-122">NOTES</span></span>

## <span data-ttu-id="2fa53-123">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2fa53-123">RELATED LINKS</span></span>
