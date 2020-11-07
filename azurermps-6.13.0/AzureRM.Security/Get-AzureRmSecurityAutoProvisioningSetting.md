---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityAutoProvisioningSetting.md
ms.openlocfilehash: 98adc5714f4a4abaeca9fe6723b1a56fe1d49fca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679514"
---
# <span data-ttu-id="03fff-101">Get-AzureRmSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="03fff-101">Get-AzureRmSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="03fff-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="03fff-102">SYNOPSIS</span></span>
<span data-ttu-id="03fff-103">A biztonsági automatikus kiépítési beállítások megkeresése</span><span class="sxs-lookup"><span data-stu-id="03fff-103">Gets the security automatic provisioning settings</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03fff-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="03fff-104">SYNTAX</span></span>

### <span data-ttu-id="03fff-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="03fff-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03fff-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="03fff-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="03fff-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="03fff-107">ResourceId</span></span>
```
Get-AzureRmSecurityAutoProvisioningSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="03fff-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="03fff-108">DESCRIPTION</span></span>
<span data-ttu-id="03fff-109">Az automatikus kiépítési beállítások segítségével eldöntheti, hogy az Azure Security Cetner automatikusan proviosion-e egy olyan biztonsági ügynököt, amely telepítve lesz a VMs-eszközén.</span><span class="sxs-lookup"><span data-stu-id="03fff-109">Automatic Provisioning Settings let you decide whether you want Azure Security Cetner to automatically proviosion a security agent that will be installed on your VMs.</span></span>
<span data-ttu-id="03fff-110">A biztonsági ügynök figyeli a VM-et biztonsági riasztások létrehozásához és a VM biztonsági megfelelőségének figyeléséhez.</span><span class="sxs-lookup"><span data-stu-id="03fff-110">The security agent will monitor your VM to create security alerts and monitor the security compliance of the VM.</span></span>

## <span data-ttu-id="03fff-111">Példák</span><span class="sxs-lookup"><span data-stu-id="03fff-111">EXAMPLES</span></span>

### <span data-ttu-id="03fff-112">Példa 1</span><span class="sxs-lookup"><span data-stu-id="03fff-112">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityAutoProvisioningSetting -Name "default"
Id                                                                                                                Name    AutoProvision
--                                                                                                                ----    -------------
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/autoProvisioningSettings/default default On
```

<span data-ttu-id="03fff-113">Az előfizetés automatikus kiépítési beállítása</span><span class="sxs-lookup"><span data-stu-id="03fff-113">Gets the auto provisioning setting for the subscription</span></span>

## <span data-ttu-id="03fff-114">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="03fff-114">PARAMETERS</span></span>

### <span data-ttu-id="03fff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03fff-115">-DefaultProfile</span></span>
<span data-ttu-id="03fff-116">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="03fff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fff-117">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="03fff-117">-Name</span></span>
<span data-ttu-id="03fff-118">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="03fff-118">Resource name.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03fff-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="03fff-119">-ResourceId</span></span>
<span data-ttu-id="03fff-120">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="03fff-120">Resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03fff-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03fff-121">CommonParameters</span></span>
<span data-ttu-id="03fff-122">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="03fff-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03fff-123">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03fff-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03fff-124">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="03fff-124">INPUTS</span></span>

### <span data-ttu-id="03fff-125">System. String</span><span class="sxs-lookup"><span data-stu-id="03fff-125">System.String</span></span>

## <span data-ttu-id="03fff-126">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="03fff-126">OUTPUTS</span></span>

### <span data-ttu-id="03fff-127">Microsoft. Azure. commands. Security. models. AutoProvisioningSettings. PSSecurityAutoProvisioningSetting</span><span class="sxs-lookup"><span data-stu-id="03fff-127">Microsoft.Azure.Commands.Security.Models.AutoProvisioningSettings.PSSecurityAutoProvisioningSetting</span></span>

## <span data-ttu-id="03fff-128">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="03fff-128">NOTES</span></span>

## <span data-ttu-id="03fff-129">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="03fff-129">RELATED LINKS</span></span>
