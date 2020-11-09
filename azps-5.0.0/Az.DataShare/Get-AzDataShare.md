---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: a4c63e22427e3ae0b666bb7d99b8217a990657c2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297554"
---
# <span data-ttu-id="4a832-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4a832-101">Get-AzDataShare</span></span>

## <span data-ttu-id="4a832-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4a832-102">SYNOPSIS</span></span>
<span data-ttu-id="4a832-103">Információkat kaphat az adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4a832-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="4a832-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4a832-104">SYNTAX</span></span>

### <span data-ttu-id="4a832-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4a832-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a832-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4a832-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a832-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4a832-107">DESCRIPTION</span></span>
<span data-ttu-id="4a832-108">A **Get-AzDataShare** parancsmag az Azure-adatmegosztási accoount az adatmegosztásokra vonatkozó információkat kap.</span><span class="sxs-lookup"><span data-stu-id="4a832-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="4a832-109">Ha megadja az adatmegosztás nevét, ez a parancsmag információkat kap az adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4a832-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="4a832-110">Ha nem ad meg nevet, ez a parancsmag információkat kap az Azure-adatmegosztási fiókban található összes adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4a832-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="4a832-111">Példák</span><span class="sxs-lookup"><span data-stu-id="4a832-111">EXAMPLES</span></span>

### <span data-ttu-id="4a832-112">Példa 1: konkrét adatmegosztás beszerzése</span><span class="sxs-lookup"><span data-stu-id="4a832-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="4a832-113">Ez a parancs információkat jelenít meg az Azure adatmegosztási fiók WikiAdsAccount és az erőforráscsoport HIRDETÉSEIben tárolt AdsShare.</span><span class="sxs-lookup"><span data-stu-id="4a832-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="4a832-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4a832-114">PARAMETERS</span></span>

### <span data-ttu-id="4a832-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4a832-115">-AccountName</span></span>
<span data-ttu-id="4a832-116">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="4a832-116">Azure data share account name</span></span>

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

### <span data-ttu-id="4a832-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a832-117">-DefaultProfile</span></span>
<span data-ttu-id="4a832-118">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4a832-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a832-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="4a832-119">-Name</span></span>
<span data-ttu-id="4a832-120">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="4a832-120">Azure data share name</span></span>

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

### <span data-ttu-id="4a832-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a832-121">-ResourceGroupName</span></span>
<span data-ttu-id="4a832-122">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="4a832-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4a832-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4a832-123">-ResourceId</span></span>
<span data-ttu-id="4a832-124">Az Azure-adatmegosztás erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4a832-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="4a832-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a832-125">CommonParameters</span></span>
<span data-ttu-id="4a832-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4a832-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a832-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4a832-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a832-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a832-128">INPUTS</span></span>

### <span data-ttu-id="4a832-129">System. String</span><span class="sxs-lookup"><span data-stu-id="4a832-129">System.String</span></span>

## <span data-ttu-id="4a832-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4a832-130">OUTPUTS</span></span>

### <span data-ttu-id="4a832-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4a832-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4a832-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4a832-132">NOTES</span></span>

## <span data-ttu-id="4a832-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4a832-133">RELATED LINKS</span></span>
