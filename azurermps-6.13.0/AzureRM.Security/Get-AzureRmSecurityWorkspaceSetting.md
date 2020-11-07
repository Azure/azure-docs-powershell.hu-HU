---
external help file: Microsoft.Azure.Commands.SecurityCenter.dll-Help.xml
Module Name: AzureRM.Security
online version: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Security/Commands.Security/help/Get-AzureRmSecurityWorkspaceSetting.md
ms.openlocfilehash: 7e2a655810c885245d3694fb63caa44c5b4119e1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93672902"
---
# <span data-ttu-id="9c5df-101">Get-AzureRmSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9c5df-101">Get-AzureRmSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9c5df-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9c5df-102">SYNOPSIS</span></span>
<span data-ttu-id="9c5df-103">A beállított biztonsági munkaterület beállításainak lekérdezése az előfizetésben.</span><span class="sxs-lookup"><span data-stu-id="9c5df-103">Gets the configured security workspace settings on a subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c5df-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9c5df-104">SYNTAX</span></span>

### <span data-ttu-id="9c5df-105">SubscriptionScope (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="9c5df-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmSecurityWorkspaceSetting [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c5df-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="9c5df-106">SubscriptionLevelResource</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9c5df-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c5df-107">ResourceId</span></span>
```
Get-AzureRmSecurityWorkspaceSetting -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c5df-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="9c5df-108">DESCRIPTION</span></span>
<span data-ttu-id="9c5df-109">Ezzel a parancsmaggal megkeresheti azt a beállított munkaterületet, amely az előfizetésben a VMs-szolgáltatónál telepített biztonsági ügynök által összegyűjtött biztonsági adatokat fogja tárolni.</span><span class="sxs-lookup"><span data-stu-id="9c5df-109">This cmdlet lets you discover the configured workspace that will hold the security data that was collected by the security agent that is installed in VMs inside this subscription.</span></span>

## <span data-ttu-id="9c5df-110">Példák</span><span class="sxs-lookup"><span data-stu-id="9c5df-110">EXAMPLES</span></span>

### <span data-ttu-id="9c5df-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="9c5df-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSecurityWorkspaceSetting

Id                                                                                                         Name    WorkspaceId                                                                                                                               
--                                                                                                         ----    -----------                                                                                                                               
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/workspaceSettings/default default /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/resourcegroups/mainws/providers/microsoft.operationalinsights/workspaces/securityus...
```

<span data-ttu-id="9c5df-112">Az előfizetéshez tartozó munkaterület-beállításokat kapja.</span><span class="sxs-lookup"><span data-stu-id="9c5df-112">Gets the workspace settings for a subscription.</span></span>

## <span data-ttu-id="9c5df-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9c5df-113">PARAMETERS</span></span>

### <span data-ttu-id="9c5df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c5df-114">-DefaultProfile</span></span>
<span data-ttu-id="9c5df-115">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9c5df-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c5df-116">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="9c5df-116">-Name</span></span>
<span data-ttu-id="9c5df-117">Erőforrás neve</span><span class="sxs-lookup"><span data-stu-id="9c5df-117">Resource name.</span></span>

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

### <span data-ttu-id="9c5df-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c5df-118">-ResourceId</span></span>
<span data-ttu-id="9c5df-119">Erőforrás-azonosító.</span><span class="sxs-lookup"><span data-stu-id="9c5df-119">Resource ID.</span></span>

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

### <span data-ttu-id="9c5df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c5df-120">CommonParameters</span></span>
<span data-ttu-id="9c5df-121">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9c5df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c5df-122">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c5df-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c5df-123">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5df-123">INPUTS</span></span>

### <span data-ttu-id="9c5df-124">System. String</span><span class="sxs-lookup"><span data-stu-id="9c5df-124">System.String</span></span>

## <span data-ttu-id="9c5df-125">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9c5df-125">OUTPUTS</span></span>

### <span data-ttu-id="9c5df-126">Microsoft. Azure. commands. Security. models. WorkspaceSettings. PSSecurityWorkspaceSetting</span><span class="sxs-lookup"><span data-stu-id="9c5df-126">Microsoft.Azure.Commands.Security.Models.WorkspaceSettings.PSSecurityWorkspaceSetting</span></span>

## <span data-ttu-id="9c5df-127">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9c5df-127">NOTES</span></span>

## <span data-ttu-id="9c5df-128">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9c5df-128">RELATED LINKS</span></span>
