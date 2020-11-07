---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: 8c0df920b8619760cf4a80d9ef6502e82de9a31f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668188"
---
# <span data-ttu-id="f123c-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="f123c-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="f123c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f123c-102">SYNOPSIS</span></span>
<span data-ttu-id="f123c-103">Értesítési előzményeket kap az adatokról</span><span class="sxs-lookup"><span data-stu-id="f123c-103">Gets Alert History information</span></span>

## <span data-ttu-id="f123c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f123c-104">SYNTAX</span></span>

### <span data-ttu-id="f123c-105">ByAlertId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f123c-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f123c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f123c-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f123c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="f123c-107">DESCRIPTION</span></span>
<span data-ttu-id="f123c-108">A **Get-AzAlertObjectHistory** parancsmag a riasztások előzményeit kapja meg.</span><span class="sxs-lookup"><span data-stu-id="f123c-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="f123c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="f123c-109">EXAMPLES</span></span>

### <span data-ttu-id="f123c-110">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f123c-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="f123c-111">Értesítési előzmények adatainak megjelenítése</span><span class="sxs-lookup"><span data-stu-id="f123c-111">Gets alert history details.</span></span> 

## <span data-ttu-id="f123c-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f123c-112">PARAMETERS</span></span>

### <span data-ttu-id="f123c-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="f123c-113">-AlertId</span></span>
<span data-ttu-id="f123c-114">Értesítési/ResourceId egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="f123c-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="f123c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f123c-115">-DefaultProfile</span></span>
<span data-ttu-id="f123c-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f123c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f123c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f123c-117">-InputObject</span></span>
<span data-ttu-id="f123c-118">Bemeneti objektum a pipeline-ról</span><span class="sxs-lookup"><span data-stu-id="f123c-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="f123c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f123c-119">CommonParameters</span></span>
<span data-ttu-id="f123c-120">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f123c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f123c-121">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f123c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f123c-122">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f123c-122">INPUTS</span></span>

### <span data-ttu-id="f123c-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="f123c-123">None</span></span>

## <span data-ttu-id="f123c-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f123c-124">OUTPUTS</span></span>

### <span data-ttu-id="f123c-125">Microsoft. Azure. Command. AlertsManagement. OutputModels. PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="f123c-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="f123c-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f123c-126">NOTES</span></span>

## <span data-ttu-id="f123c-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f123c-127">RELATED LINKS</span></span>
