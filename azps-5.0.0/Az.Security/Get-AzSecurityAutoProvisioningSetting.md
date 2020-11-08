---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 08631f5705a3a0255c42ac3d146cef45de1b4e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94188016"
---
# <span data-ttu-id="f7683-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="f7683-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="f7683-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f7683-102">SYNOPSIS</span></span>
<span data-ttu-id="f7683-103">A biztonsági automatikus kiépítési beállítások megkeresése</span><span class="sxs-lookup"><span data-stu-id="f7683-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="f7683-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f7683-104">SYNTAX</span></span>

### <span data-ttu-id="f7683-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="f7683-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f7683-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="f7683-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f7683-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7683-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f7683-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="f7683-108">DESCRIPTION</span></span>
<span data-ttu-id="f7683-109">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Center automatikusan nyújt-e olyan biztonsági ügynököt, amely a VMs-eszközön lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="f7683-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="f7683-110">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="f7683-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="f7683-111">Példák</span><span class="sxs-lookup"><span data-stu-id="f7683-111">EXAMPLES</span></span>

### <span data-ttu-id="f7683-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f7683-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="f7683-113">Az előfizetés automatikus kiépítési beállítása</span><span class="sxs-lookup"><span data-stu-id="f7683-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="f7683-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f7683-114">PARAMETERS</span></span>

### <span data-ttu-id="f7683-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7683-115">-DefaultProfile</span></span>
<span data-ttu-id="f7683-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f7683-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7683-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="f7683-117">-Name</span></span>
<span data-ttu-id="f7683-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="f7683-118">Resource name.</span></span>

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

### <span data-ttu-id="f7683-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7683-119">-ResourceId</span></span>
<span data-ttu-id="f7683-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="f7683-120">Resource ID.</span></span>

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

### <span data-ttu-id="f7683-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7683-121">CommonParameters</span></span>
<span data-ttu-id="f7683-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f7683-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7683-123">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f7683-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7683-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7683-124">INPUTS</span></span>

### <span data-ttu-id="f7683-125">System. String</span><span class="sxs-lookup"><span data-stu-id="f7683-125">System.String</span></span>

## <span data-ttu-id="f7683-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f7683-126">OUTPUTS</span></span>

### <span data-ttu-id="f7683-127">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="f7683-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="f7683-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f7683-128">NOTES</span></span>

## <span data-ttu-id="f7683-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f7683-129">RELATED LINKS</span></span>