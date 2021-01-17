---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationDetail.md
ms.openlocfilehash: 2ee3714895b751223768ac3f98efbd04405ae69f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98342042"
---
# <span data-ttu-id="61615-101">Get-AzDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="61615-101">Get-AzDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="61615-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61615-102">SYNOPSIS</span></span>
<span data-ttu-id="61615-103">Információkat kap a megosztás szinkronizálási részleteiről.</span><span class="sxs-lookup"><span data-stu-id="61615-103">Gets information about synchronization details for a share.</span></span>

## <span data-ttu-id="61615-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="61615-104">SYNTAX</span></span>

### <span data-ttu-id="61615-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="61615-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationDetail -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 -SynchronizationId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="61615-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="61615-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationDetail -SynchronizationId <String> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="61615-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="61615-107">DESCRIPTION</span></span>
<span data-ttu-id="61615-108">A **Get-AzDataShareSynchronizationDetail** parancsmag a megosztáshoz kezdeményezett szinkronizálás részleteit tartalmazza.</span><span class="sxs-lookup"><span data-stu-id="61615-108">The **Get-AzDataShareSynchronizationDetail** cmdlet provides details of the synchronization initiated for a share.</span></span>

## <span data-ttu-id="61615-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="61615-109">EXAMPLES</span></span>

### <span data-ttu-id="61615-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="61615-110">Example 1</span></span>
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

<span data-ttu-id="61615-111">Ez a parancs információt nyújt a megadott szinkronizálási azonosítónak megfelelő összes adatkészlet szinkronizálási részleteiről.</span><span class="sxs-lookup"><span data-stu-id="61615-111">This command provides information about the synchronization details of all the data sets corresponding to the provided synchronization id.</span></span>

## <span data-ttu-id="61615-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61615-112">PARAMETERS</span></span>

### <span data-ttu-id="61615-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61615-113">-AccountName</span></span>
<span data-ttu-id="61615-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="61615-114">Azure data share account name</span></span>

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

### <span data-ttu-id="61615-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61615-115">-DefaultProfile</span></span>
<span data-ttu-id="61615-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="61615-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61615-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61615-117">-ResourceGroupName</span></span>
<span data-ttu-id="61615-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="61615-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="61615-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="61615-119">-ResourceId</span></span>
<span data-ttu-id="61615-120">Azure-adatok megosztása erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="61615-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="61615-121">-ShareName</span><span class="sxs-lookup"><span data-stu-id="61615-121">-ShareName</span></span>
<span data-ttu-id="61615-122">Azure-adatok megosztásának neve</span><span class="sxs-lookup"><span data-stu-id="61615-122">Azure data share name</span></span>

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

### <span data-ttu-id="61615-123">-SynchronizationId</span><span class="sxs-lookup"><span data-stu-id="61615-123">-SynchronizationId</span></span>
<span data-ttu-id="61615-124">A megosztási szinkronizálás szinkronizálási azonosítója</span><span class="sxs-lookup"><span data-stu-id="61615-124">Synchronization id of share synchronization</span></span>

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

### <span data-ttu-id="61615-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61615-125">CommonParameters</span></span>
<span data-ttu-id="61615-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61615-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61615-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61615-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61615-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61615-128">INPUTS</span></span>

### <span data-ttu-id="61615-129">System.String</span><span class="sxs-lookup"><span data-stu-id="61615-129">System.String</span></span>

## <span data-ttu-id="61615-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="61615-130">OUTPUTS</span></span>

### <span data-ttu-id="61615-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span><span class="sxs-lookup"><span data-stu-id="61615-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationDetail</span></span>

## <span data-ttu-id="61615-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="61615-132">NOTES</span></span>

## <span data-ttu-id="61615-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="61615-133">RELATED LINKS</span></span>
