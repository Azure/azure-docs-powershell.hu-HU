---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 679b1458b3e749b2ccfca3863f745edd562ffc2f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93669221"
---
# <span data-ttu-id="5ec10-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5ec10-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5ec10-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="5ec10-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec10-103">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="5ec10-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="5ec10-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="5ec10-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec10-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="5ec10-105">DESCRIPTION</span></span>
<span data-ttu-id="5ec10-106">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="5ec10-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="5ec10-107">A beállított munkaterület az előfizetésben a VMs-szolgáltatónál telepített biztonsági ügynök által gyűjtött biztonsági adatokat fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="5ec10-107">The configured workspace will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="5ec10-108">Példák</span><span class="sxs-lookup"><span data-stu-id="5ec10-108">EXAMPLES</span></span>

### <span data-ttu-id="5ec10-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="5ec10-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="5ec10-110">A "myWorkspace" munkaterület beállítása a biztonsági ügynökök által gyűjtött összes biztonsági adatok tárolásához.</span><span class="sxs-lookup"><span data-stu-id="5ec10-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the security agents.</span></span>

## <span data-ttu-id="5ec10-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="5ec10-111">PARAMETERS</span></span>

### <span data-ttu-id="5ec10-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec10-112">-DefaultProfile</span></span>
<span data-ttu-id="5ec10-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5ec10-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec10-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="5ec10-114">-Name</span></span>
<span data-ttu-id="5ec10-115">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="5ec10-115">Resource name.</span></span>

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

### <span data-ttu-id="5ec10-116">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="5ec10-116">-Scope</span></span>
<span data-ttu-id="5ec10-117">Hatókör.</span><span class="sxs-lookup"><span data-stu-id="5ec10-117">Scope.</span></span>

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

### <span data-ttu-id="5ec10-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="5ec10-118">-WorkspaceId</span></span>
<span data-ttu-id="5ec10-119">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="5ec10-119">Workspace ID.</span></span>

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

### <span data-ttu-id="5ec10-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="5ec10-120">-Confirm</span></span>
<span data-ttu-id="5ec10-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="5ec10-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec10-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec10-122">-WhatIf</span></span>
<span data-ttu-id="5ec10-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="5ec10-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ec10-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="5ec10-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec10-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec10-125">CommonParameters</span></span>
<span data-ttu-id="5ec10-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="5ec10-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec10-127">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ec10-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec10-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec10-128">INPUTS</span></span>

### <span data-ttu-id="5ec10-129">System. String</span><span class="sxs-lookup"><span data-stu-id="5ec10-129">System.String</span></span>

## <span data-ttu-id="5ec10-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5ec10-130">OUTPUTS</span></span>

### <span data-ttu-id="5ec10-131">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="5ec10-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="5ec10-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="5ec10-132">NOTES</span></span>

## <span data-ttu-id="5ec10-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5ec10-133">RELATED LINKS</span></span>
