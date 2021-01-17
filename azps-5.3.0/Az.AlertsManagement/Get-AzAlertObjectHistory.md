---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/get-azalertobjecthistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Get-AzAlertObjectHistory.md
ms.openlocfilehash: bf2062ab320c02bbb3f29c038161ddcb4342675f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469085"
---
# <span data-ttu-id="567d2-101">Get-AzAlertObjectHistory</span><span class="sxs-lookup"><span data-stu-id="567d2-101">Get-AzAlertObjectHistory</span></span>

## <span data-ttu-id="567d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="567d2-102">SYNOPSIS</span></span>
<span data-ttu-id="567d2-103">Értesítési előzményinformációk lekérte</span><span class="sxs-lookup"><span data-stu-id="567d2-103">Gets Alert History information</span></span>

## <span data-ttu-id="567d2-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="567d2-104">SYNTAX</span></span>

### <span data-ttu-id="567d2-105">ByAlertId (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="567d2-105">ByAlertId (Default)</span></span>
```
Get-AzAlertObjectHistory -AlertId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="567d2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="567d2-106">ByInputObject</span></span>
```
Get-AzAlertObjectHistory -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="567d2-107">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="567d2-107">DESCRIPTION</span></span>
<span data-ttu-id="567d2-108">**A Get-AzAlertObjectHistory** parancsmag riasztási előzményeket kap.</span><span class="sxs-lookup"><span data-stu-id="567d2-108">**Get-AzAlertObjectHistory** cmdlet gets history of alert.</span></span>

## <span data-ttu-id="567d2-109">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="567d2-109">EXAMPLES</span></span>

### <span data-ttu-id="567d2-110">1. példa</span><span class="sxs-lookup"><span data-stu-id="567d2-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAlertObjectHistory -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529"
```

<span data-ttu-id="567d2-111">A riasztási előzmények részleteinek megtekintése.</span><span class="sxs-lookup"><span data-stu-id="567d2-111">Gets alert history details.</span></span> 

## <span data-ttu-id="567d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="567d2-112">PARAMETERS</span></span>

### <span data-ttu-id="567d2-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="567d2-113">-AlertId</span></span>
<span data-ttu-id="567d2-114">Riasztás/Erőforrásazonosító egyedi azonosítója.</span><span class="sxs-lookup"><span data-stu-id="567d2-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="567d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="567d2-115">-DefaultProfile</span></span>
<span data-ttu-id="567d2-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="567d2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="567d2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="567d2-117">-InputObject</span></span>
<span data-ttu-id="567d2-118">Input object from pipeline.</span><span class="sxs-lookup"><span data-stu-id="567d2-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="567d2-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="567d2-119">CommonParameters</span></span>
<span data-ttu-id="567d2-120">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="567d2-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="567d2-121">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="567d2-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="567d2-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="567d2-122">INPUTS</span></span>

### <span data-ttu-id="567d2-123">Nincs</span><span class="sxs-lookup"><span data-stu-id="567d2-123">None</span></span>

## <span data-ttu-id="567d2-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="567d2-124">OUTPUTS</span></span>

### <span data-ttu-id="567d2-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span><span class="sxs-lookup"><span data-stu-id="567d2-125">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlertModification</span></span>

## <span data-ttu-id="567d2-126">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="567d2-126">NOTES</span></span>

## <span data-ttu-id="567d2-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="567d2-127">RELATED LINKS</span></span>
