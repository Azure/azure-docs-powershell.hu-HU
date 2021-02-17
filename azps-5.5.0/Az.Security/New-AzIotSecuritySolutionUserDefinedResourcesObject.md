---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208311"
---
# <span data-ttu-id="4b362-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="4b362-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="4b362-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b362-102">SYNOPSIS</span></span>
<span data-ttu-id="4b362-103">Új felhasználói erőforrások létrehozása az iot biztonsági megoldáshoz</span><span class="sxs-lookup"><span data-stu-id="4b362-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="4b362-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="4b362-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b362-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="4b362-105">DESCRIPTION</span></span>
<span data-ttu-id="4b362-106">AzIotSecuritySolutionUserDefinedResourcesObject parancsmag létrehoz egy új felhasználó által definiált erőforrás-objektumot az iot biztonsági megoldáshoz.</span><span class="sxs-lookup"><span data-stu-id="4b362-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="4b362-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="4b362-107">EXAMPLES</span></span>

### <span data-ttu-id="4b362-108">1. példa</span><span class="sxs-lookup"><span data-stu-id="4b362-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="4b362-109">Új felhasználói erőforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="4b362-109">Create new user defined resources</span></span>

## <span data-ttu-id="4b362-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b362-110">PARAMETERS</span></span>

### <span data-ttu-id="4b362-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b362-111">-DefaultProfile</span></span>
<span data-ttu-id="4b362-112">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4b362-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b362-113">-Query</span><span class="sxs-lookup"><span data-stu-id="4b362-113">-Query</span></span>
<span data-ttu-id="4b362-114">Lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="4b362-114">Query.</span></span>

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

### <span data-ttu-id="4b362-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="4b362-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="4b362-116">Lekérdezési előfizetések.</span><span class="sxs-lookup"><span data-stu-id="4b362-116">Query subscriptions.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b362-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b362-117">CommonParameters</span></span>
<span data-ttu-id="4b362-118">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b362-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b362-119">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b362-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b362-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b362-120">INPUTS</span></span>

### <span data-ttu-id="4b362-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="4b362-121">None</span></span>

## <span data-ttu-id="4b362-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4b362-122">OUTPUTS</span></span>

### <span data-ttu-id="4b362-123">Microsoft.Azure.Commands.Security.Models.iotSecuritySolutions.PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="4b362-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="4b362-124">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="4b362-124">NOTES</span></span>

## <span data-ttu-id="4b362-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4b362-125">RELATED LINKS</span></span>
