---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/New-AzIotSecuritySolutionUserDefinedResourcesObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/New-AzIotSecuritySolutionUserDefinedResourcesObject.md
ms.openlocfilehash: e824c32ae2ae4f28972cdac9446eeeae6e410c75
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94195515"
---
# <span data-ttu-id="35778-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span><span class="sxs-lookup"><span data-stu-id="35778-101">New-AzIotSecuritySolutionUserDefinedResourcesObject</span></span>

## <span data-ttu-id="35778-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35778-102">SYNOPSIS</span></span>
<span data-ttu-id="35778-103">Új felhasználó által definiált erőforrások létrehozása a IOT biztonsági megoldásához</span><span class="sxs-lookup"><span data-stu-id="35778-103">Create new user defined resources for iot security solution</span></span>

## <span data-ttu-id="35778-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35778-104">SYNTAX</span></span>

```
New-AzIotSecuritySolutionUserDefinedResourcesObject -Query <String> -QuerySubscriptionList <String[]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="35778-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="35778-105">DESCRIPTION</span></span>
<span data-ttu-id="35778-106">A AzIotSecuritySolutionUserDefinedResourcesObject parancsmag létrehoz egy új, felhasználó által definiált erőforrás-objektumot a IOT biztonsági megoldásához.</span><span class="sxs-lookup"><span data-stu-id="35778-106">The AzIotSecuritySolutionUserDefinedResourcesObject cmdlet creates a new user defined resources object for the iot security solution.</span></span>

## <span data-ttu-id="35778-107">Példák</span><span class="sxs-lookup"><span data-stu-id="35778-107">EXAMPLES</span></span>

### <span data-ttu-id="35778-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35778-108">Example 1</span></span>
```powershell
PS C:\> New-AzIotSecuritySolutionUserDefinedResourcesObject -Query 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
-QuerySubscriptionList @("XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX")

Query: 'where type != "microsoft.devices/iothubs" | where name contains "v2"' 
QuerySubscriptions: ["XXXXXXXX-XXXX-XXXXX-XXXX-XXXXXXXXXXXX"]
```

<span data-ttu-id="35778-109">Új felhasználó által definiált erőforrások létrehozása</span><span class="sxs-lookup"><span data-stu-id="35778-109">Create new user defined resources</span></span>

## <span data-ttu-id="35778-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35778-110">PARAMETERS</span></span>

### <span data-ttu-id="35778-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35778-111">-DefaultProfile</span></span>
<span data-ttu-id="35778-112">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35778-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35778-113">-Query</span><span class="sxs-lookup"><span data-stu-id="35778-113">-Query</span></span>
<span data-ttu-id="35778-114">Lekérdezés.</span><span class="sxs-lookup"><span data-stu-id="35778-114">Query.</span></span>

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

### <span data-ttu-id="35778-115">-QuerySubscriptionList</span><span class="sxs-lookup"><span data-stu-id="35778-115">-QuerySubscriptionList</span></span>
<span data-ttu-id="35778-116">Lekérdezési előfizetések.</span><span class="sxs-lookup"><span data-stu-id="35778-116">Query subscriptions.</span></span>

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

### <span data-ttu-id="35778-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35778-117">CommonParameters</span></span>
<span data-ttu-id="35778-118">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35778-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35778-119">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="35778-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35778-120">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35778-120">INPUTS</span></span>

### <span data-ttu-id="35778-121">Nincs</span><span class="sxs-lookup"><span data-stu-id="35778-121">None</span></span>

## <span data-ttu-id="35778-122">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35778-122">OUTPUTS</span></span>

### <span data-ttu-id="35778-123">Microsoft. Azure. commands. Security. models. IotSecuritySolutions. PSUserDefinedResources</span><span class="sxs-lookup"><span data-stu-id="35778-123">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSUserDefinedResources</span></span>

## <span data-ttu-id="35778-124">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35778-124">NOTES</span></span>

## <span data-ttu-id="35778-125">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35778-125">RELATED LINKS</span></span>
