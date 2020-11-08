---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 5b905083668392ce026bfa416252eb1371ebb640
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94011589"
---
# <span data-ttu-id="34088-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="34088-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="34088-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="34088-102">SYNOPSIS</span></span>
<span data-ttu-id="34088-103">A beállított biztonsági munkaterület beállításainak lekérdezése az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="34088-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="34088-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="34088-104">SYNTAX</span></span>

### <span data-ttu-id="34088-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="34088-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34088-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="34088-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34088-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="34088-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="34088-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="34088-108">DESCRIPTION</span></span>
<span data-ttu-id="34088-109">Ezzel a parancsmaggal megkeresheti azt a beállított munkaterületet, amely az előfizetésben a VMs-szolgáltatónál telepített biztonsági ügynök által összegyűjtött biztonsági adatokat fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="34088-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="34088-110">Példák</span><span class="sxs-lookup"><span data-stu-id="34088-110">EXAMPLES</span></span>

### <span data-ttu-id="34088-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="34088-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="34088-112">Az előfizetéshez tartozó munkaterület-beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="34088-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="34088-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="34088-113">PARAMETERS</span></span>

### <span data-ttu-id="34088-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34088-114">-DefaultProfile</span></span>
<span data-ttu-id="34088-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="34088-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34088-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="34088-116">-Name</span></span>
<span data-ttu-id="34088-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="34088-117">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34088-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="34088-118">-ResourceId</span></span>
<span data-ttu-id="34088-119">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="34088-119">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34088-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34088-120">CommonParameters</span></span>
<span data-ttu-id="34088-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="34088-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34088-122">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34088-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34088-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="34088-123">INPUTS</span></span>

### <span data-ttu-id="34088-124">System. String</span><span class="sxs-lookup"><span data-stu-id="34088-124">System.String</span></span>

## <span data-ttu-id="34088-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="34088-125">OUTPUTS</span></span>

### <span data-ttu-id="34088-126">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="34088-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="34088-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="34088-127">NOTES</span></span>

## <span data-ttu-id="34088-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="34088-128">RELATED LINKS</span></span>
