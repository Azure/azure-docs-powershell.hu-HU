---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: 8a80277508f9cd2998668185af6a8c0b5bbec128
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923754"
---
# <span data-ttu-id="5cca9-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="5cca9-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="5cca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cca9-102">SYNOPSIS</span></span>
<span data-ttu-id="5cca9-103">Információkat kap a megosztási előfizetésben futtatott szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="5cca9-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="5cca9-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5cca9-104">SYNTAX</span></span>

### <span data-ttu-id="5cca9-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="5cca9-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5cca9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5cca9-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5cca9-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5cca9-107">DESCRIPTION</span></span>
<span data-ttu-id="5cca9-108">A **Get-AzDataShareSubscriptionSynchronization** parancsmag informaitont biztosít minden szinkronizálásról, amely egy megosztási előfizetésben a felhasználó adatmegosztási fiókjában fut.</span><span class="sxs-lookup"><span data-stu-id="5cca9-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="5cca9-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5cca9-109">EXAMPLES</span></span>

### <span data-ttu-id="5cca9-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="5cca9-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="5cca9-111">Ez a parancs információkat nyújt a share-előfizetéshez futtatott AdsShareSubscription szinkronizálásról a WikiAds adatmegosztási fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="5cca9-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="5cca9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5cca9-112">PARAMETERS</span></span>

### <span data-ttu-id="5cca9-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="5cca9-113">-AccountName</span></span>
<span data-ttu-id="5cca9-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="5cca9-114">Azure data share account name</span></span>

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

### <span data-ttu-id="5cca9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cca9-115">-DefaultProfile</span></span>
<span data-ttu-id="5cca9-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5cca9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5cca9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cca9-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cca9-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="5cca9-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="5cca9-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cca9-119">-ResourceId</span></span>
<span data-ttu-id="5cca9-120">Azure data share subscription resource id</span><span class="sxs-lookup"><span data-stu-id="5cca9-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="5cca9-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="5cca9-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="5cca9-122">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="5cca9-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="5cca9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cca9-123">CommonParameters</span></span>
<span data-ttu-id="5cca9-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cca9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cca9-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5cca9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cca9-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5cca9-126">INPUTS</span></span>

### <span data-ttu-id="5cca9-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5cca9-127">System.String</span></span>

## <span data-ttu-id="5cca9-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5cca9-128">OUTPUTS</span></span>

### <span data-ttu-id="5cca9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="5cca9-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="5cca9-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5cca9-130">NOTES</span></span>

## <span data-ttu-id="5cca9-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5cca9-131">RELATED LINKS</span></span>
