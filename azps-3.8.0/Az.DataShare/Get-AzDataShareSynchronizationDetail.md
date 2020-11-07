---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 8e0f62f4b3d29d0aff9a2bdfcd7916805544af14
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846289"
---
# <span data-ttu-id="cf717-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="cf717-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="cf717-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cf717-102">SYNOPSIS</span></span>
<span data-ttu-id="cf717-103">Információt kap egy megosztás szinkronizálási részleteiről.</span><span class="sxs-lookup"><span data-stu-id="cf717-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="cf717-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cf717-104">SYNTAX</span></span>

### <span data-ttu-id="cf717-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cf717-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cf717-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cf717-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cf717-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="cf717-107">DESCRIPTION</span></span>
<span data-ttu-id="cf717-108">A **Get-AzDataShareSynchronizationDetail** parancsmag részleteket tartalmaz a megosztáshoz kezdeményezett szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="cf717-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="cf717-109">Példák</span><span class="sxs-lookup"><span data-stu-id="cf717-109">EXAMPLES</span></span>

### <span data-ttu-id="cf717-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cf717-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationDetail -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -SynchronizationId "02a17faa-4498-45ee-a884-162180af9251"

DataSetId    : d2411889-5357-4ca8-8d65-9363e46ef2ed
DataSetType  : BlobFolder
EndTime      : 7/8/2019 10:24:27 PM
StartTime    : 7/8/2019 10:23:09 PM
Status       : Succeeded
DurationMs   : 78870
FilesRead    : 1
FilesWritten : 1
SizeRead     : 2779935
SizeWritten  : 2779935
Name         : 16d5161b-2b3f-4d90-b074-13ad7121bcc7
Message      :
```

<span data-ttu-id="cf717-111">Ez a parancs információkat nyújt a megadott szinkronizálási azonosítóhoz tartozó összes adathalmaz szinkronizálási részleteiről.</span><span class="sxs-lookup"><span data-stu-id="cf717-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="cf717-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cf717-112">PARAMETERS</span></span>

### <span data-ttu-id="cf717-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="cf717-113">-AccountName</span></span>
<span data-ttu-id="cf717-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="cf717-114">Azure data share account name</span></span>

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

### <span data-ttu-id="cf717-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf717-115">-DefaultProfile</span></span>
<span data-ttu-id="cf717-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cf717-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cf717-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf717-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf717-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="cf717-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="cf717-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cf717-119">-ResourceId</span></span>
<span data-ttu-id="cf717-120">Azure Data Share Resource id</span><span class="sxs-lookup"><span data-stu-id="cf717-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="cf717-121">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="cf717-121">-ShareName</span></span>
<span data-ttu-id="cf717-122">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="cf717-122">Azure data share name</span></span>

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

### <span data-ttu-id="cf717-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="cf717-123">-SynchronizationId</span></span>
<span data-ttu-id="cf717-124">A megosztási szinkronizálás szinkronizálási azonosítója</span><span class="sxs-lookup"><span data-stu-id="cf717-124">Synchronization id of share synchronization</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cf717-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf717-125">CommonParameters</span></span>
<span data-ttu-id="cf717-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cf717-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf717-127">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf717-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf717-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf717-128">INPUTS</span></span>

### <span data-ttu-id="cf717-129">System. String</span><span class="sxs-lookup"><span data-stu-id="cf717-129">System.String</span></span>

## <span data-ttu-id="cf717-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cf717-130">OUTPUTS</span></span>

### <span data-ttu-id="cf717-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="cf717-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="cf717-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cf717-132">NOTES</span></span>

## <span data-ttu-id="cf717-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cf717-133">RELATED LINKS</span></span>
