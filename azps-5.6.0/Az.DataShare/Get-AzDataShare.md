---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatashare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShare.md
ms.openlocfilehash: 1cccba1d3af4bcd1ff69ad04f248615e1edb66fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942610"
---
# <span data-ttu-id="4448c-101">Get-AzDataShare</span><span class="sxs-lookup"><span data-stu-id="4448c-101">Get-AzDataShare</span></span>

## <span data-ttu-id="4448c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4448c-102">SYNOPSIS</span></span>
<span data-ttu-id="4448c-103">Információ az adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4448c-103">Get information about Data Shares.</span></span>

## <span data-ttu-id="4448c-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4448c-104">SYNTAX</span></span>

### <span data-ttu-id="4448c-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4448c-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShare -ResourceGroupName <String> -AccountName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4448c-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4448c-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShare -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4448c-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4448c-107">DESCRIPTION</span></span>
<span data-ttu-id="4448c-108">A **Get-AzDataShare** parancsmag információkat kap egy Azure-adatmegosztási accoount adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4448c-108">The **Get-AzDataShare** cmdlet gets information about data shares in an Azure data share accoount.</span></span>
<span data-ttu-id="4448c-109">Ha megadja egy adat megosztás nevét, ez a parancsmag információt kap az adat megosztásáról.</span><span class="sxs-lookup"><span data-stu-id="4448c-109">If you specify the name of a data share, this cmdlet gets information about that data share.</span></span>
<span data-ttu-id="4448c-110">Ha nem ad meg nevet, ez a parancsmag információt kap egy Azure-alapú adatmegosztási fiók összes adatmegosztási lehetőségével kapcsolatban.</span><span class="sxs-lookup"><span data-stu-id="4448c-110">If you do not specify a name, this cmdlet gets information about all of the data shares in an Azure data share account.</span></span>

## <span data-ttu-id="4448c-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4448c-111">EXAMPLES</span></span>

### <span data-ttu-id="4448c-112">1. példa: Konkrét adat-megosztás</span><span class="sxs-lookup"><span data-stu-id="4448c-112">Example 1 : Get a specific data share</span></span>
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

<span data-ttu-id="4448c-113">Ez a parancs információkat jelenít meg az Azure-adatmegosztási fiók WikiAdsAccount és erőforráscsoport ADS szolgáltatásában található AdsShare adatmegosztásról.</span><span class="sxs-lookup"><span data-stu-id="4448c-113">This command displays information about data share AdsShare in the Azure data share account WikiAdsAccount and resource group ADS.</span></span>

## <span data-ttu-id="4448c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4448c-114">PARAMETERS</span></span>

### <span data-ttu-id="4448c-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="4448c-115">-AccountName</span></span>
<span data-ttu-id="4448c-116">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="4448c-116">Azure data share account name</span></span>

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

### <span data-ttu-id="4448c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4448c-117">-DefaultProfile</span></span>
<span data-ttu-id="4448c-118">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4448c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4448c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4448c-119">-Name</span></span>
<span data-ttu-id="4448c-120">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="4448c-120">Azure data share name</span></span>

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

### <span data-ttu-id="4448c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4448c-121">-ResourceGroupName</span></span>
<span data-ttu-id="4448c-122">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="4448c-122">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="4448c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4448c-123">-ResourceId</span></span>
<span data-ttu-id="4448c-124">Az Azure-adat megosztásának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="4448c-124">The resource id of the azure data share</span></span>

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

### <span data-ttu-id="4448c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4448c-125">CommonParameters</span></span>
<span data-ttu-id="4448c-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4448c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4448c-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4448c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4448c-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4448c-128">INPUTS</span></span>

### <span data-ttu-id="4448c-129">System.String</span><span class="sxs-lookup"><span data-stu-id="4448c-129">System.String</span></span>

## <span data-ttu-id="4448c-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4448c-130">OUTPUTS</span></span>

### <span data-ttu-id="4448c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span><span class="sxs-lookup"><span data-stu-id="4448c-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShare</span></span>

## <span data-ttu-id="4448c-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4448c-132">NOTES</span></span>

## <span data-ttu-id="4448c-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4448c-133">RELATED LINKS</span></span>
