---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024989"
---
# <span data-ttu-id="8eca4-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="8eca4-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="8eca4-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="8eca4-102">SYNOPSIS</span></span>
<span data-ttu-id="8eca4-103">Értesítési előzményeket kap az adatokról</span><span class="sxs-lookup"><span data-stu-id="8eca4-103">Gets Alert History information</span></span>

## <span data-ttu-id="8eca4-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="8eca4-104">SYNTAX</span></span>

### <span data-ttu-id="8eca4-105">ByAlertId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="8eca4-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8eca4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8eca4-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8eca4-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="8eca4-107">DESCRIPTION</span></span>
<span data-ttu-id="8eca4-108">A **Get-AzAlertObjectHistory** parancsmag a riasztások előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="8eca4-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="8eca4-109">Példák</span><span class="sxs-lookup"><span data-stu-id="8eca4-109">EXAMPLES</span></span>

### <span data-ttu-id="8eca4-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="8eca4-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="8eca4-111">Értesítési előzmények adatainak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="8eca4-111">Gets alert history details.</span></span> 

## <span data-ttu-id="8eca4-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="8eca4-112">PARAMETERS</span></span>

### <span data-ttu-id="8eca4-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="8eca4-113">-AlertId</span></span>
<span data-ttu-id="8eca4-114">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="8eca4-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eca4-115">-DefaultProfile</span></span>
<span data-ttu-id="8eca4-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="8eca4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8eca4-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8eca4-117">-InputObject</span></span>
<span data-ttu-id="8eca4-118">Bemeneti objektum a pipeline-ról</span><span class="sxs-lookup"><span data-stu-id="8eca4-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eca4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eca4-119">CommonParameters</span></span>
<span data-ttu-id="8eca4-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="8eca4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eca4-121">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="8eca4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eca4-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="8eca4-122">INPUTS</span></span>

### <span data-ttu-id="8eca4-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="8eca4-123">None</span></span>

## <span data-ttu-id="8eca4-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="8eca4-124">OUTPUTS</span></span>

### <span data-ttu-id="8eca4-125">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="8eca4-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="8eca4-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="8eca4-126">NOTES</span></span>

## <span data-ttu-id="8eca4-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="8eca4-127">RELATED LINKS</span></span>
