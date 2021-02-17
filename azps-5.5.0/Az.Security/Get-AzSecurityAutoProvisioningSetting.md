---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165163"
---
# <span data-ttu-id="60cc4-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="60cc4-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="60cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="60cc4-103">A biztonsági automatikus kiépítési beállítások lekérte</span><span class="sxs-lookup"><span data-stu-id="60cc4-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="60cc4-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="60cc4-104">SYNTAX</span></span>

### <span data-ttu-id="60cc4-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="60cc4-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="60cc4-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="60cc4-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="60cc4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="60cc4-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60cc4-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="60cc4-108">DESCRIPTION</span></span>
<span data-ttu-id="60cc4-109">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy szeretné-e, hogy az Azure Biztonsági központ automatikusan kiépítsen egy biztonsági ügynököt, amely telepítve lesz a virtuális gépekre.</span><span class="sxs-lookup"><span data-stu-id="60cc4-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="60cc4-110">A biztonsági ügynök figyeli a vm-et, és biztonsági riasztásokat hoz létre, és figyeli a virtuális gép biztonsági megfelelőségét.</span><span class="sxs-lookup"><span data-stu-id="60cc4-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="60cc4-111">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="60cc4-111">EXAMPLES</span></span>

### <span data-ttu-id="60cc4-112">1. példa</span><span class="sxs-lookup"><span data-stu-id="60cc4-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="60cc4-113">Az előfizetés automatikus kiépítési beállításának lekérte</span><span class="sxs-lookup"><span data-stu-id="60cc4-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="60cc4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60cc4-114">PARAMETERS</span></span>

### <span data-ttu-id="60cc4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60cc4-115">-DefaultProfile</span></span>
<span data-ttu-id="60cc4-116">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="60cc4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60cc4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="60cc4-117">-Name</span></span>
<span data-ttu-id="60cc4-118">Erőforrás neve.</span><span class="sxs-lookup"><span data-stu-id="60cc4-118">Resource name.</span></span>

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

### <span data-ttu-id="60cc4-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="60cc4-119">-ResourceId</span></span>
<span data-ttu-id="60cc4-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="60cc4-120">Resource ID.</span></span>

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

### <span data-ttu-id="60cc4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60cc4-121">CommonParameters</span></span>
<span data-ttu-id="60cc4-122">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60cc4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60cc4-123">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60cc4-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60cc4-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="60cc4-124">INPUTS</span></span>

### <span data-ttu-id="60cc4-125">System.String</span><span class="sxs-lookup"><span data-stu-id="60cc4-125">System.String</span></span>

## <span data-ttu-id="60cc4-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="60cc4-126">OUTPUTS</span></span>

### <span data-ttu-id="60cc4-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="60cc4-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="60cc4-128">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="60cc4-128">NOTES</span></span>

## <span data-ttu-id="60cc4-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="60cc4-129">RELATED LINKS</span></span>
