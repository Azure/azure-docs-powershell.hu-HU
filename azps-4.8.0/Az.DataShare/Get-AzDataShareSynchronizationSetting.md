---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronizationsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronizationSetting.md
ms.openlocfilehash: 183164c3f2a18e68b9eab3f505f382a161abf415
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94182814"
---
# <span data-ttu-id="963ee-101">Get-AzDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="963ee-101">Get-AzDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="963ee-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="963ee-102">SYNOPSIS</span></span>
<span data-ttu-id="963ee-103">Információt kap a megosztás szinkronizálási beállításairól.</span><span class="sxs-lookup"><span data-stu-id="963ee-103">Gets information about synchronization setting on a share.</span></span>

## <span data-ttu-id="963ee-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="963ee-104">SYNTAX</span></span>

### <span data-ttu-id="963ee-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="963ee-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="963ee-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="963ee-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronizationSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="963ee-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="963ee-107">DESCRIPTION</span></span>
<span data-ttu-id="963ee-108">A **Get-AzDataShareSynchronizationSetting** parancsmag információkat nyújt a megosztásban engedélyezett szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="963ee-108">The **Get-AzDataShareSynchronizationSetting** cmdlet provides information about synchronization enabled on a share.</span></span> 

## <span data-ttu-id="963ee-109">Példák</span><span class="sxs-lookup"><span data-stu-id="963ee-109">EXAMPLES</span></span>

### <span data-ttu-id="963ee-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="963ee-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronizationSetting -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare" -Name "ShareSynchronization"

RecurrenceInterval  : Day
SynchronizationTime : 7/9/2019 9:00:00 AM
ProvisioningState   : Succeeded
CreatedAt           : 7/10/2019 12:01:08 AM
CreatedBy           : ADS Test
Id                  : /subscriptions/1834da9b-787a-44f6-ae81-60707ab8c957/resourceGroups/ADS/providers/Microsoft.
                      DataShare/accounts/WikiAds/shares/AdShare/synchronizationSettings/ShareSynchronization
Name                : ShareSynchronization
Type                : Microsoft.DataShare/SynchronizationSettings
```

<span data-ttu-id="963ee-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds az adatmegosztási ShareSynchronization engedélyezve AdsShare-szinkronizálási.</span><span class="sxs-lookup"><span data-stu-id="963ee-111">This command provides information about synchronization ShareSynchronization enabled on share AdsShare under data share account WikiAds.</span></span>

## <span data-ttu-id="963ee-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="963ee-112">PARAMETERS</span></span>

### <span data-ttu-id="963ee-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="963ee-113">-AccountName</span></span>
<span data-ttu-id="963ee-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="963ee-114">Azure data share account name</span></span>

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

### <span data-ttu-id="963ee-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="963ee-115">-DefaultProfile</span></span>
<span data-ttu-id="963ee-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="963ee-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="963ee-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="963ee-117">-Name</span></span>
<span data-ttu-id="963ee-118">A szinkronizálási beállítás neve</span><span class="sxs-lookup"><span data-stu-id="963ee-118">Name for Synchronization Setting</span></span>

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

### <span data-ttu-id="963ee-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="963ee-119">-ResourceGroupName</span></span>
<span data-ttu-id="963ee-120">Az Azure Data Share-fiók erőforrás-csoportjának neve</span><span class="sxs-lookup"><span data-stu-id="963ee-120">Resource group name of azure data share account</span></span>

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

### <span data-ttu-id="963ee-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="963ee-121">-ResourceId</span></span>
<span data-ttu-id="963ee-122">Az Azure Data Share szinkronizálási beállításának erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="963ee-122">The resource id of the azure data share synchronization setting</span></span>

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

### <span data-ttu-id="963ee-123">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="963ee-123">-ShareName</span></span>
<span data-ttu-id="963ee-124">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="963ee-124">Azure data share name</span></span>

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

### <span data-ttu-id="963ee-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="963ee-125">CommonParameters</span></span>
<span data-ttu-id="963ee-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="963ee-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="963ee-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="963ee-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="963ee-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="963ee-128">INPUTS</span></span>

### <span data-ttu-id="963ee-129">System. String</span><span class="sxs-lookup"><span data-stu-id="963ee-129">System.String</span></span>

## <span data-ttu-id="963ee-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="963ee-130">OUTPUTS</span></span>

### <span data-ttu-id="963ee-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span><span class="sxs-lookup"><span data-stu-id="963ee-131">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronizationSetting</span></span>

## <span data-ttu-id="963ee-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="963ee-132">NOTES</span></span>

## <span data-ttu-id="963ee-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="963ee-133">RELATED LINKS</span></span>
