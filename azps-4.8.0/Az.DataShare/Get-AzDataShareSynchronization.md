---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: b60b43b2c0a28be969ad633c80338f42b2c98db6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183647"
---
# <span data-ttu-id="094a1-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="094a1-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="094a1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="094a1-102">SYNOPSIS</span></span>
<span data-ttu-id="094a1-103">Információt kap egy megosztás szinkronizálási beállításáról.</span><span class="sxs-lookup"><span data-stu-id="094a1-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="094a1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="094a1-104">SYNTAX</span></span>

### <span data-ttu-id="094a1-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="094a1-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="094a1-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="094a1-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="094a1-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="094a1-107">DESCRIPTION</span></span>
<span data-ttu-id="094a1-108">A **Get-AzDataShareSynchronization** parancsmag információkat nyújt az adatmegosztási fiók csoportban lévő megosztási beállításokról.</span><span class="sxs-lookup"><span data-stu-id="094a1-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="094a1-109">Példák</span><span class="sxs-lookup"><span data-stu-id="094a1-109">EXAMPLES</span></span>

### <span data-ttu-id="094a1-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="094a1-110">Example 1</span></span>
```
PS C:\> Get-AzDataShareSynchronization -ResourceGroupName "ADS" -AccountName "WikiAds" -ShareName "AdsShare"

Company           : ADS Test
DurationMs        : 107013
EndTime           : 7/8/2019 11:53:18 PM
Message           :
StartTime         : 7/8/2019 11:51:34 PM
Status            : Succeeded
SynchronizationId : e6dc7080-6589-4628-8b50-8fc31b460089
```

<span data-ttu-id="094a1-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds megosztási AdsShare az összes szinkronizálási beállításról.</span><span class="sxs-lookup"><span data-stu-id="094a1-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="094a1-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="094a1-112">PARAMETERS</span></span>

### <span data-ttu-id="094a1-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="094a1-113">-AccountName</span></span>
<span data-ttu-id="094a1-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="094a1-114">Azure data share account name</span></span>

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

### <span data-ttu-id="094a1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="094a1-115">-DefaultProfile</span></span>
<span data-ttu-id="094a1-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="094a1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="094a1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="094a1-117">-ResourceGroupName</span></span>
<span data-ttu-id="094a1-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="094a1-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="094a1-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="094a1-119">-ResourceId</span></span>
<span data-ttu-id="094a1-120">Azure Data Share Resource id</span><span class="sxs-lookup"><span data-stu-id="094a1-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="094a1-121">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="094a1-121">-ShareName</span></span>
<span data-ttu-id="094a1-122">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="094a1-122">Azure data share name</span></span>

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

### <span data-ttu-id="094a1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="094a1-123">CommonParameters</span></span>
<span data-ttu-id="094a1-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="094a1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="094a1-125">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="094a1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="094a1-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="094a1-126">INPUTS</span></span>

### <span data-ttu-id="094a1-127">System. String</span><span class="sxs-lookup"><span data-stu-id="094a1-127">System.String</span></span>

## <span data-ttu-id="094a1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="094a1-128">OUTPUTS</span></span>

### <span data-ttu-id="094a1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="094a1-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="094a1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="094a1-130">NOTES</span></span>

## <span data-ttu-id="094a1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="094a1-131">RELATED LINKS</span></span>
