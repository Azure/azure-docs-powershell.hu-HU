---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94185019"
---
# <span data-ttu-id="d004f-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d004f-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d004f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d004f-102">SYNOPSIS</span></span>
<span data-ttu-id="d004f-103">A szinkronizálásról szóló információkat a megosztási előfizetésben futtatja.</span><span class="sxs-lookup"><span data-stu-id="d004f-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="d004f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d004f-104">SYNTAX</span></span>

### <span data-ttu-id="d004f-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d004f-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d004f-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d004f-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d004f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d004f-107">DESCRIPTION</span></span>
<span data-ttu-id="d004f-108">A **Get-AzDataShareSubscriptionSynchronization** parancsmag a felhasználó adatmegosztási fiókja alatt futó megosztási előfizetésben informaiton nyújt.</span><span class="sxs-lookup"><span data-stu-id="d004f-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="d004f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d004f-109">EXAMPLES</span></span>

### <span data-ttu-id="d004f-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="d004f-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="d004f-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds az AdsShareSubscription-előfizetés megosztási verziójában futó összes szinkronizálási műveletről.</span><span class="sxs-lookup"><span data-stu-id="d004f-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="d004f-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d004f-112">PARAMETERS</span></span>

### <span data-ttu-id="d004f-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d004f-113">-AccountName</span></span>
<span data-ttu-id="d004f-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="d004f-114">Azure data share account name</span></span>

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

### <span data-ttu-id="d004f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d004f-115">-DefaultProfile</span></span>
<span data-ttu-id="d004f-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d004f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d004f-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d004f-117">-ResourceGroupName</span></span>
<span data-ttu-id="d004f-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="d004f-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="d004f-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d004f-119">-ResourceId</span></span>
<span data-ttu-id="d004f-120">Azure Data Share-előfizetés erőforrás-azonosítója</span><span class="sxs-lookup"><span data-stu-id="d004f-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="d004f-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="d004f-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="d004f-122">Azure Data Share-előfizetés neve</span><span class="sxs-lookup"><span data-stu-id="d004f-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="d004f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d004f-123">CommonParameters</span></span>
<span data-ttu-id="d004f-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d004f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d004f-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="d004f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d004f-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d004f-126">INPUTS</span></span>

### <span data-ttu-id="d004f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d004f-127">System.String</span></span>

## <span data-ttu-id="d004f-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d004f-128">OUTPUTS</span></span>

### <span data-ttu-id="d004f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="d004f-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="d004f-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d004f-130">NOTES</span></span>

## <span data-ttu-id="d004f-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d004f-131">RELATED LINKS</span></span>
