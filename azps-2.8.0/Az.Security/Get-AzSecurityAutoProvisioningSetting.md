---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAutoProvisioningSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 988bff314b43791648ce5d42c827bfcb38e1f5b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93838085"
---
# <span data-ttu-id="35515-101">Get-AzSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="35515-101">Get-AzSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="35515-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="35515-102">SYNOPSIS</span></span>
<span data-ttu-id="35515-103">A biztonsági automatikus kiépítési beállítások megkeresése</span><span class="sxs-lookup"><span data-stu-id="35515-103">Gets the security automatic provisioning settings</span></span>

## <span data-ttu-id="35515-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="35515-104">SYNTAX</span></span>

### <span data-ttu-id="35515-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="35515-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="35515-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="35515-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35515-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="35515-107">ResourceId</span></span>
```
Get-AzSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35515-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="35515-108">DESCRIPTION</span></span>
<span data-ttu-id="35515-109">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Center automatikusan nyújt-e olyan biztonsági ügynököt, amely a VMs-eszközön lesz telepítve.</span><span class="sxs-lookup"><span data-stu-id="35515-109">Automatic Provisioning Settings let you decide whether you want Azure Security Center to automatically provision a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="35515-110">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="35515-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="35515-111">Példák</span><span class="sxs-lookup"><span data-stu-id="35515-111">EXAMPLES</span></span>

### <span data-ttu-id="35515-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="35515-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="35515-113">Az előfizetés automatikus kiépítési beállítása</span><span class="sxs-lookup"><span data-stu-id="35515-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="35515-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="35515-114">PARAMETERS</span></span>

### <span data-ttu-id="35515-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35515-115">-DefaultProfile</span></span>
<span data-ttu-id="35515-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="35515-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35515-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="35515-117">-Name</span></span>
<span data-ttu-id="35515-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="35515-118">Resource name.</span></span>

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

### <span data-ttu-id="35515-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="35515-119">-ResourceId</span></span>
<span data-ttu-id="35515-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="35515-120">Resource ID.</span></span>

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

### <span data-ttu-id="35515-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35515-121">CommonParameters</span></span>
<span data-ttu-id="35515-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="35515-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35515-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35515-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35515-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="35515-124">INPUTS</span></span>

### <span data-ttu-id="35515-125">System. String</span><span class="sxs-lookup"><span data-stu-id="35515-125">System.String</span></span>

## <span data-ttu-id="35515-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="35515-126">OUTPUTS</span></span>

### <span data-ttu-id="35515-127">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="35515-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="35515-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="35515-128">NOTES</span></span>

## <span data-ttu-id="35515-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="35515-129">RELATED LINKS</span></span>
