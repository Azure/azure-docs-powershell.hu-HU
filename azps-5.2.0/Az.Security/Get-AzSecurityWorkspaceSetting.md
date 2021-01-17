---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: ca4f0d39b0023d641e2f95ceb4eddf90f19a51f1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337433"
---
# <span data-ttu-id="2d2b7-101">Get-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2d2b7-101">Get-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2d2b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2b7-103">Az előfizetéshez beállított biztonsági munkaterület-beállításokat kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-103">Gets the configured security workspace settings on a subscription.</span></span>

## <span data-ttu-id="2d2b7-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2d2b7-104">SYNTAX</span></span>

### <span data-ttu-id="2d2b7-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2d2b7-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2b7-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="2d2b7-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2d2b7-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d2b7-107">ResourceId</span></span>
```
Get-AzSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d2b7-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2d2b7-108">DESCRIPTION</span></span>
<span data-ttu-id="2d2b7-109">Ezzel a parancsmaggal felfedezheti azt a konfigurált munkaterületet, amely az előfizetésen belül telepített biztonsági ügynök által gyűjtött biztonsági adatokat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="2d2b7-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2d2b7-110">EXAMPLES</span></span>

### <span data-ttu-id="2d2b7-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="2d2b7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="2d2b7-112">Az előfizetés munkaterületi beállításait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="2d2b7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d2b7-113">PARAMETERS</span></span>

### <span data-ttu-id="2d2b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2b7-114">-DefaultProfile</span></span>
<span data-ttu-id="2d2b7-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d2b7-116">-Name</span><span class="sxs-lookup"><span data-stu-id="2d2b7-116">-Name</span></span>
<span data-ttu-id="2d2b7-117">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-117">Resource name.</span></span>

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

### <span data-ttu-id="2d2b7-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2d2b7-118">-ResourceId</span></span>
<span data-ttu-id="2d2b7-119">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-119">Resource ID.</span></span>

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

### <span data-ttu-id="2d2b7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2b7-120">CommonParameters</span></span>
<span data-ttu-id="2d2b7-121">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2b7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2b7-122">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d2b7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2b7-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2d2b7-123">INPUTS</span></span>

### <span data-ttu-id="2d2b7-124">System.String</span><span class="sxs-lookup"><span data-stu-id="2d2b7-124">System.String</span></span>

## <span data-ttu-id="2d2b7-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2d2b7-125">OUTPUTS</span></span>

### <span data-ttu-id="2d2b7-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2d2b7-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2d2b7-127">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2d2b7-127">NOTES</span></span>

## <span data-ttu-id="2d2b7-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2d2b7-128">RELATED LINKS</span></span>
