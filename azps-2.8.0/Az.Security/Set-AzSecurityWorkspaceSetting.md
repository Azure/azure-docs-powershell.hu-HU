---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: c425a7d11fab8bc019ca3944d034dfa2bfb96d06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838828"
---
# <span data-ttu-id="f0707-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f0707-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f0707-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f0707-102">SYNOPSIS</span></span>
<span data-ttu-id="f0707-103">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="f0707-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="f0707-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f0707-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0707-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f0707-105">DESCRIPTION</span></span>
<span data-ttu-id="f0707-106">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="f0707-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="f0707-107">A beállított munkaterület azokat a biztonsági adatokat fogja tárolni, amelyeket az Azure log Analytics Agent Agent az előfizetésben telepített VMs-szolgáltatónál telepített.</span><span class="sxs-lookup"><span data-stu-id="f0707-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="f0707-108">Példák</span><span class="sxs-lookup"><span data-stu-id="f0707-108">EXAMPLES</span></span>

### <span data-ttu-id="f0707-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f0707-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="f0707-110">A "myWorkspace" munkaterület beállítása az Azure log Analytics-ügynök által gyűjtött összes biztonsági adatok tárolásához.</span><span class="sxs-lookup"><span data-stu-id="f0707-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="f0707-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f0707-111">PARAMETERS</span></span>

### <span data-ttu-id="f0707-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0707-112">-DefaultProfile</span></span>
<span data-ttu-id="f0707-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f0707-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0707-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f0707-114">-Name</span></span>
<span data-ttu-id="f0707-115">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f0707-115">Resource name.</span></span>

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

### <span data-ttu-id="f0707-116">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="f0707-116">-Scope</span></span>
<span data-ttu-id="f0707-117">Hatókör.</span><span class="sxs-lookup"><span data-stu-id="f0707-117">Scope.</span></span>

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

### <span data-ttu-id="f0707-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="f0707-118">-WorkspaceId</span></span>
<span data-ttu-id="f0707-119">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f0707-119">Workspace ID.</span></span>

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

### <span data-ttu-id="f0707-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f0707-120">-Confirm</span></span>
<span data-ttu-id="f0707-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f0707-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0707-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0707-122">-WhatIf</span></span>
<span data-ttu-id="f0707-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f0707-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f0707-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f0707-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0707-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0707-125">CommonParameters</span></span>
<span data-ttu-id="f0707-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f0707-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0707-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0707-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0707-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0707-128">INPUTS</span></span>

### <span data-ttu-id="f0707-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f0707-129">System.String</span></span>

## <span data-ttu-id="f0707-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f0707-130">OUTPUTS</span></span>

### <span data-ttu-id="f0707-131">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="f0707-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="f0707-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f0707-132">NOTES</span></span>

## <span data-ttu-id="f0707-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f0707-133">RELATED LINKS</span></span>
