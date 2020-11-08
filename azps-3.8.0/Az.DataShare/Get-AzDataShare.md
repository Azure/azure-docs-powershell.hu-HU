---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a01d67a5ebf98e07a9410903e4c00b4ed4ee70a2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94010964"
---
# <span data-ttu-id="cb5aa-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="cb5aa-101">Get-AzDataShare</span></span>

## <span data-ttu-id="cb5aa-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cb5aa-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5aa-103">Információkat kaphat az adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="cb5aa-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cb5aa-104">SYNTAX</span></span>

### <span data-ttu-id="cb5aa-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cb5aa-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cb5aa-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb5aa-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb5aa-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cb5aa-107">DESCRIPTION</span></span>
<span data-ttu-id="cb5aa-108">A **Get-AzDataShare** parancsmag az Azure-adatmegosztási accoount az adatmegosztásokra vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="cb5aa-109">Ha megadja az adatmegosztás nevét, ez a parancsmag információkat kap az adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="cb5aa-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az Azure-adatmegosztási fiókban található összes adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="cb5aa-111">Példák</span><span class="sxs-lookup"><span data-stu-id="cb5aa-111">EXAMPLES</span></span>

### <span data-ttu-id="cb5aa-112">Példa 1: konkrét adatmegosztás beszerzése</span><span class="sxs-lookup"><span data-stu-id="cb5aa-112">Example 1 : Get a specific data share</span></span>
```
PS C:\>Get-AzDataShare -ResourceGroupName "ADS" -AccountName "WikiAdsAccount" -Name "AdsShare"
Name                : AdsShare
Id                  : /subscriptions/f3ead1ff-d0ab-4cf4-9a5a-86f1661d4685/resourceGroups/ADS/providers/Microsoft.DataShare/accounts/WikiAdsAccount/shares/AdsShare
Type                : Microsoft.DataShare/shares
CreatedAt           : 6/11/2019 12:00:00 AM
CreatedBy           : Contoso ADS
ShareKind           : CopyBased
Description         : Example of description  
ProvisioningState   : Succeeded
Terms               : This should not be shared
```

<span data-ttu-id="cb5aa-113">Ez a parancs információkat jelenít meg az Azure adatmegosztási fiók WikiAdsAccount és az erőforráscsoport HIRDETÉSEIben tárolt AdsShare.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="cb5aa-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cb5aa-114">PARAMETERS</span></span>

### <span data-ttu-id="cb5aa-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cb5aa-115">-AccountName</span></span>
<span data-ttu-id="cb5aa-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="cb5aa-116">Azure data share account name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5aa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5aa-117">-DefaultProfile</span></span>
<span data-ttu-id="cb5aa-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cb5aa-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cb5aa-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cb5aa-119">-Name</span></span>
<span data-ttu-id="cb5aa-120">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="cb5aa-120">Azure data share name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5aa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5aa-121">-ResourceGroupName</span></span>
<span data-ttu-id="cb5aa-122">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="cb5aa-122">The resource group name of the azure data share account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5aa-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb5aa-123">-ResourceId</span></span>
<span data-ttu-id="cb5aa-124">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="cb5aa-124">The resource id of the azure data share</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5aa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5aa-125">CommonParameters</span></span>
<span data-ttu-id="cb5aa-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cb5aa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5aa-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb5aa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5aa-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb5aa-128">INPUTS</span></span>

### <span data-ttu-id="cb5aa-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cb5aa-129">System.String</span></span>

## <span data-ttu-id="cb5aa-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cb5aa-130">OUTPUTS</span></span>

### <span data-ttu-id="cb5aa-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="cb5aa-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="cb5aa-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cb5aa-132">NOTES</span></span>

## <span data-ttu-id="cb5aa-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cb5aa-133">RELATED LINKS</span></span>
