---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: a02d2685987844db5f88fafaf12d0c9aed4a3234
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169019"
---
# <span data-ttu-id="2c1ea-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2c1ea-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2c1ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="2c1ea-103">Frissíti az előfizetés munkaterületi beállításait.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="2c1ea-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="2c1ea-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c1ea-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="2c1ea-105">DESCRIPTION</span></span>
<span data-ttu-id="2c1ea-106">Frissíti az előfizetés munkaterületi beállításait.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="2c1ea-107">A konfigurált munkaterület az ebben az előfizetésben lévő virtuális gépekre telepített Azure Log Analytics ügynök által gyűjtött biztonsági adatokat fogja tartalmazni.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="2c1ea-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="2c1ea-108">EXAMPLES</span></span>

### <span data-ttu-id="2c1ea-109">1. példa</span><span class="sxs-lookup"><span data-stu-id="2c1ea-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="2c1ea-110">A "securityuserws" munkaterületet úgy állítja be, hogy az Azure Log Analytics-ügynök által gyűjtött összes biztonsági adatot megtartsa.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-110">Sets the "securityuserws" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="2c1ea-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c1ea-111">PARAMETERS</span></span>

### <span data-ttu-id="2c1ea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c1ea-112">-DefaultProfile</span></span>
<span data-ttu-id="2c1ea-113">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c1ea-114">-Name</span><span class="sxs-lookup"><span data-stu-id="2c1ea-114">-Name</span></span>
<span data-ttu-id="2c1ea-115">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-115">Resource name.</span></span>

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

### <span data-ttu-id="2c1ea-116">-Scope</span><span class="sxs-lookup"><span data-stu-id="2c1ea-116">-Scope</span></span>
<span data-ttu-id="2c1ea-117">Hatókör.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-117">Scope.</span></span>

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

### <span data-ttu-id="2c1ea-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="2c1ea-118">-WorkspaceId</span></span>
<span data-ttu-id="2c1ea-119">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-119">Workspace ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c1ea-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c1ea-120">-Confirm</span></span>
<span data-ttu-id="2c1ea-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c1ea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c1ea-122">-WhatIf</span></span>
<span data-ttu-id="2c1ea-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c1ea-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c1ea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c1ea-125">CommonParameters</span></span>
<span data-ttu-id="2c1ea-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c1ea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c1ea-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c1ea-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c1ea-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2c1ea-128">INPUTS</span></span>

### <span data-ttu-id="2c1ea-129">System.String</span><span class="sxs-lookup"><span data-stu-id="2c1ea-129">System.String</span></span>

## <span data-ttu-id="2c1ea-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2c1ea-130">OUTPUTS</span></span>

### <span data-ttu-id="2c1ea-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="2c1ea-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="2c1ea-132">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="2c1ea-132">NOTES</span></span>

## <span data-ttu-id="2c1ea-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2c1ea-133">RELATED LINKS</span></span>
