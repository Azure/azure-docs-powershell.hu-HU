---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: a719d841df2d3f211fdb2592ed2a96b507c51e10
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841977"
---
# <span data-ttu-id="2429e-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="2429e-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="2429e-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2429e-102">SYNOPSIS</span></span>
<span data-ttu-id="2429e-103">Automatikusan létrehoz egy automéretarányos webkampót.</span><span class="sxs-lookup"><span data-stu-id="2429e-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="2429e-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2429e-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2429e-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="2429e-105">DESCRIPTION</span></span>
<span data-ttu-id="2429e-106">A **New-AzAutoscaleWebhook** parancsmag automéretarányos webkampót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="2429e-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="2429e-107">Példák</span><span class="sxs-lookup"><span data-stu-id="2429e-107">EXAMPLES</span></span>

## <span data-ttu-id="2429e-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2429e-108">PARAMETERS</span></span>

### <span data-ttu-id="2429e-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2429e-109">-DefaultProfile</span></span>
<span data-ttu-id="2429e-110">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés</span><span class="sxs-lookup"><span data-stu-id="2429e-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2429e-111">-Tulajdonság</span><span class="sxs-lookup"><span data-stu-id="2429e-111">-Property</span></span>
<span data-ttu-id="2429e-112">A @ formátum @ (property1 = "érték1",....) tulajdonságainak listáját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2429e-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2429e-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="2429e-113">-ServiceUri</span></span>
<span data-ttu-id="2429e-114">A szolgáltatás URI-jét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2429e-114">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2429e-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2429e-115">CommonParameters</span></span>
<span data-ttu-id="2429e-116">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2429e-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2429e-117">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="2429e-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2429e-118">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2429e-118">INPUTS</span></span>

### <span data-ttu-id="2429e-119">System. String</span><span class="sxs-lookup"><span data-stu-id="2429e-119">System.String</span></span>

### <span data-ttu-id="2429e-120">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="2429e-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2429e-121">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2429e-121">OUTPUTS</span></span>

### <span data-ttu-id="2429e-122">Microsoft. Azure. Management. monitor. Management. models. WebhookNotification</span><span class="sxs-lookup"><span data-stu-id="2429e-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="2429e-123">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2429e-123">NOTES</span></span>

## <span data-ttu-id="2429e-124">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2429e-124">RELATED LINKS</span></span>

[<span data-ttu-id="2429e-125">Új – AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="2429e-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


