---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Set-AzSecurityWorkspaceSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Set-AzSecurityWorkspaceSetting.md
ms.openlocfilehash: 23d35a0bce62aa2a3a5c922ea0e25e35cb619b09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186192"
---
# <span data-ttu-id="fec74-101">Set-AzSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="fec74-101">Set-AzSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="fec74-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="fec74-102">SYNOPSIS</span></span>
<span data-ttu-id="fec74-103">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="fec74-103">Updates the workspace settings for the subscription.</span></span>

## <span data-ttu-id="fec74-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="fec74-104">SYNTAX</span></span>

```
Set-AzSecurityWorkspaceSetting -Name <String> -Scope <String> -WorkspaceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec74-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="fec74-105">DESCRIPTION</span></span>
<span data-ttu-id="fec74-106">Az előfizetés munkaterület-beállításainak frissítése.</span><span class="sxs-lookup"><span data-stu-id="fec74-106">Updates the workspace settings for the subscription.</span></span>
<span data-ttu-id="fec74-107">A beállított munkaterület azokat a biztonsági adatokat fogja tárolni, amelyeket az Azure log Analytics Agent Agent az előfizetésben telepített VMs-szolgáltatónál telepített.</span><span class="sxs-lookup"><span data-stu-id="fec74-107">The configured workspace will hold the security data that was collected by the Azure Log Analytics agent agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="fec74-108">Példák</span><span class="sxs-lookup"><span data-stu-id="fec74-108">EXAMPLES</span></span>

### <span data-ttu-id="fec74-109">Példa 1</span><span class="sxs-lookup"><span data-stu-id="fec74-109">Example 1</span></span>
```powershell
PS C:\> Set-AzSecurityWorkspaceSetting -Name "default" -Scope "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869" -WorkspaceId  "/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityuserws"

Id                                                                                                         Name    WorkspaceId 
--                                                                                                         ----    ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /...
```

<span data-ttu-id="fec74-110">A "myWorkspace" munkaterület beállítása az Azure log Analytics-ügynök által gyűjtött összes biztonsági adatok tárolásához.</span><span class="sxs-lookup"><span data-stu-id="fec74-110">Sets the "myWorkspace" workspace to hold all the security data that was collected by the Azure Log Analytics agent.</span></span>

## <span data-ttu-id="fec74-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="fec74-111">PARAMETERS</span></span>

### <span data-ttu-id="fec74-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec74-112">-DefaultProfile</span></span>
<span data-ttu-id="fec74-113">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="fec74-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fec74-114">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="fec74-114">-Name</span></span>
<span data-ttu-id="fec74-115">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="fec74-115">Resource name.</span></span>

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

### <span data-ttu-id="fec74-116">-Scope (hatókör)</span><span class="sxs-lookup"><span data-stu-id="fec74-116">-Scope</span></span>
<span data-ttu-id="fec74-117">Hatókör.</span><span class="sxs-lookup"><span data-stu-id="fec74-117">Scope.</span></span>

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

### <span data-ttu-id="fec74-118">-WorkspaceId</span><span class="sxs-lookup"><span data-stu-id="fec74-118">-WorkspaceId</span></span>
<span data-ttu-id="fec74-119">Munkaterület-azonosító.</span><span class="sxs-lookup"><span data-stu-id="fec74-119">Workspace ID.</span></span>

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

### <span data-ttu-id="fec74-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="fec74-120">-Confirm</span></span>
<span data-ttu-id="fec74-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="fec74-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec74-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec74-122">-WhatIf</span></span>
<span data-ttu-id="fec74-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="fec74-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fec74-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="fec74-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec74-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec74-125">CommonParameters</span></span>
<span data-ttu-id="fec74-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="fec74-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec74-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="fec74-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec74-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="fec74-128">INPUTS</span></span>

### <span data-ttu-id="fec74-129">System. String</span><span class="sxs-lookup"><span data-stu-id="fec74-129">System.String</span></span>

## <span data-ttu-id="fec74-130">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="fec74-130">OUTPUTS</span></span>

### <span data-ttu-id="fec74-131">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="fec74-131">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="fec74-132">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="fec74-132">NOTES</span></span>

## <span data-ttu-id="fec74-133">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="fec74-133">RELATED LINKS</span></span>
