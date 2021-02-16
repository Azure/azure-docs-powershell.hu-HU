---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesubscriptionsynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSubscriptionSynchronization.md
ms.openlocfilehash: f1527cfcb947f802cb4a2710ab2f25a1d7b9bf75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163771"
---
# <span data-ttu-id="eeede-101">Get-AzDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="eeede-101">Get-AzDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="eeede-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeede-102">SYNOPSIS</span></span>
<span data-ttu-id="eeede-103">Információkat kap a megosztási előfizetésben futtatott szinkronizálásról.</span><span class="sxs-lookup"><span data-stu-id="eeede-103">Gets information about synchronization runs in share subscription.</span></span>

## <span data-ttu-id="eeede-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="eeede-104">SYNTAX</span></span>

### <span data-ttu-id="eeede-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="eeede-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceGroupName <String> -AccountName <String>
 -ShareSubscriptionName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eeede-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eeede-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSubscriptionSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="eeede-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="eeede-107">DESCRIPTION</span></span>
<span data-ttu-id="eeede-108">A **Get-AzDataShareSubscriptionSynchronization** parancsmag informaitont biztosít minden szinkronizálásról, amely egy megosztási előfizetésben a felhasználó adatmegosztási fiókjában fut.</span><span class="sxs-lookup"><span data-stu-id="eeede-108">The **Get-AzDataShareSubscriptionSynchronization** cmdlet provides informaiton about all synchronization runs in a share subscription under a data share account on the consumer.</span></span>

## <span data-ttu-id="eeede-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="eeede-109">EXAMPLES</span></span>

### <span data-ttu-id="eeede-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="eeede-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSubscriptionSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds"  -ShareSubscriptionName "AdsShareSubscription"

durationMs        : 83660
endTime           : 7/10/2019 9:01:23 AM
message           :
startTime         : 7/10/2019 9:00:04 AM
status            : Succeeded
synchronizationId : b087e1a5-9144-4e1d-86d1-2a4adcf551d4
```

<span data-ttu-id="eeede-111">Ez a parancs információkat nyújt a share-előfizetéshez futtatott AdsShareSubscription szinkronizálásról a WikiAds adatmegosztási fiók alatt.</span><span class="sxs-lookup"><span data-stu-id="eeede-111">This command provides information about all the synchronization runs for a share subscription AdsShareSubscription under data share account WikiAds.</span></span>

## <span data-ttu-id="eeede-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="eeede-112">PARAMETERS</span></span>

### <span data-ttu-id="eeede-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="eeede-113">-AccountName</span></span>
<span data-ttu-id="eeede-114">Azure data share account name</span><span class="sxs-lookup"><span data-stu-id="eeede-114">Azure data share account name</span></span>

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

### <span data-ttu-id="eeede-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeede-115">-DefaultProfile</span></span>
<span data-ttu-id="eeede-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="eeede-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eeede-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeede-117">-ResourceGroupName</span></span>
<span data-ttu-id="eeede-118">Az azure-adat-megosztási fiók erőforráscsoportneve</span><span class="sxs-lookup"><span data-stu-id="eeede-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="eeede-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eeede-119">-ResourceId</span></span>
<span data-ttu-id="eeede-120">Azure data share subscription resource id</span><span class="sxs-lookup"><span data-stu-id="eeede-120">Azure data share subscription resource id</span></span>

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

### <span data-ttu-id="eeede-121">-ShareSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="eeede-121">-ShareSubscriptionName</span></span>
<span data-ttu-id="eeede-122">Azure data share subscription name</span><span class="sxs-lookup"><span data-stu-id="eeede-122">Azure data share subscription name</span></span>

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

### <span data-ttu-id="eeede-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeede-123">CommonParameters</span></span>
<span data-ttu-id="eeede-124">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eeede-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeede-125">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="eeede-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeede-126">INPUTS</span><span class="sxs-lookup"><span data-stu-id="eeede-126">INPUTS</span></span>

### <span data-ttu-id="eeede-127">System.String</span><span class="sxs-lookup"><span data-stu-id="eeede-127">System.String</span></span>

## <span data-ttu-id="eeede-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="eeede-128">OUTPUTS</span></span>

### <span data-ttu-id="eeede-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span><span class="sxs-lookup"><span data-stu-id="eeede-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSubscriptionSynchronization</span></span>

## <span data-ttu-id="eeede-130">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="eeede-130">NOTES</span></span>

## <span data-ttu-id="eeede-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="eeede-131">RELATED LINKS</span></span>
