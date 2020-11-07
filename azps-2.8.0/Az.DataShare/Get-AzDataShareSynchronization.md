---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataShare.dll-Help.xml
Module Name: Az.DataShare
online version: https://docs.microsoft.com/en-us/powershell/module/az.datashare/get-azdatasharesynchronization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataShare/DataShare/help/Get-AzDataShareSynchronization.md
ms.openlocfilehash: f211579d98957f48a389ad10c6044c6193ad9993
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93666723"
---
# <span data-ttu-id="58a89-101">Get-AzDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="58a89-101">Get-AzDataShareSynchronization</span></span>

## <span data-ttu-id="58a89-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="58a89-102">SYNOPSIS</span></span>
<span data-ttu-id="58a89-103">Információt kap egy megosztás szinkronizálási beállításáról.</span><span class="sxs-lookup"><span data-stu-id="58a89-103">Gets information about synchronization setting for a share.</span></span>

## <span data-ttu-id="58a89-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="58a89-104">SYNTAX</span></span>

### <span data-ttu-id="58a89-105">ByFieldsParameterSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="58a89-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzDataShareSynchronization -ResourceGroupName <String> -AccountName <String> -ShareName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58a89-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58a89-106">ByResourceIdParameterSet</span></span>
```
Get-AzDataShareSynchronization -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58a89-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="58a89-107">DESCRIPTION</span></span>
<span data-ttu-id="58a89-108">A **Get-AzDataShareSynchronization** parancsmag információkat nyújt az adatmegosztási fiók csoportban lévő megosztási beállításokról.</span><span class="sxs-lookup"><span data-stu-id="58a89-108">The **Get-AzDataShareSynchronization** cmdlet provides information about all the synchronization setting present in a share under a data share account.</span></span>

## <span data-ttu-id="58a89-109">Példák</span><span class="sxs-lookup"><span data-stu-id="58a89-109">EXAMPLES</span></span>

### <span data-ttu-id="58a89-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="58a89-110">Example 1</span></span>
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

<span data-ttu-id="58a89-111">Ez a parancs információkat nyújt az adatmegosztási fiók WikiAds megosztási AdsShare az összes szinkronizálási beállításról.</span><span class="sxs-lookup"><span data-stu-id="58a89-111">This commands provides information about all synchronization settings present in share AdsShare in data share account WikiAds.</span></span>

## <span data-ttu-id="58a89-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="58a89-112">PARAMETERS</span></span>

### <span data-ttu-id="58a89-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="58a89-113">-AccountName</span></span>
<span data-ttu-id="58a89-114">Azure Data Share-fiók neve</span><span class="sxs-lookup"><span data-stu-id="58a89-114">Azure data share account name</span></span>

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

### <span data-ttu-id="58a89-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a89-115">-DefaultProfile</span></span>
<span data-ttu-id="58a89-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="58a89-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58a89-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58a89-117">-ResourceGroupName</span></span>
<span data-ttu-id="58a89-118">Az Azure Data Share-fiók erőforráscsoport-neve</span><span class="sxs-lookup"><span data-stu-id="58a89-118">The resource group name of the azure data share account</span></span>

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

### <span data-ttu-id="58a89-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58a89-119">-ResourceId</span></span>
<span data-ttu-id="58a89-120">Azure Data Share Resource id</span><span class="sxs-lookup"><span data-stu-id="58a89-120">Azure data share resource id</span></span>

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

### <span data-ttu-id="58a89-121">-Megosztásnév</span><span class="sxs-lookup"><span data-stu-id="58a89-121">-ShareName</span></span>
<span data-ttu-id="58a89-122">Azure-adatmegosztás neve</span><span class="sxs-lookup"><span data-stu-id="58a89-122">Azure data share name</span></span>

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

### <span data-ttu-id="58a89-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a89-123">CommonParameters</span></span>
<span data-ttu-id="58a89-124">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="58a89-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a89-125">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a89-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a89-126">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a89-126">INPUTS</span></span>

### <span data-ttu-id="58a89-127">System. String</span><span class="sxs-lookup"><span data-stu-id="58a89-127">System.String</span></span>

## <span data-ttu-id="58a89-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="58a89-128">OUTPUTS</span></span>

### <span data-ttu-id="58a89-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span><span class="sxs-lookup"><span data-stu-id="58a89-129">Microsoft.Azure.PowerShell.Cmdlets.DataShare.Models.PSDataShareSynchronization</span></span>

## <span data-ttu-id="58a89-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="58a89-130">NOTES</span></span>

## <span data-ttu-id="58a89-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="58a89-131">RELATED LINKS</span></span>
