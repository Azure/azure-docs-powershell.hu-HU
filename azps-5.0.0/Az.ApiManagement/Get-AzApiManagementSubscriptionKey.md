---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 227EF8A2-E04A-4F6B-B66E-E77F1276A7E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementsubscriptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementSubscriptionKey.md
ms.openlocfilehash: 74362c511abde8baed24f1b484a916a9e9851426
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301643"
---
# <span data-ttu-id="0f656-101">Get-AzApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="0f656-101">Get-AzApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="0f656-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="0f656-102">SYNOPSIS</span></span>
<span data-ttu-id="0f656-103">Előfizetési kulcsokat kap.</span><span class="sxs-lookup"><span data-stu-id="0f656-103">Gets subscription keys.</span></span>

## <span data-ttu-id="0f656-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="0f656-104">SYNTAX</span></span>

```
Get-AzApiManagementSubscriptionKey -Context <PsApiManagementContext> -SubscriptionId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f656-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="0f656-105">DESCRIPTION</span></span>
<span data-ttu-id="0f656-106">A **Get-AzApiManagementSubscriptionKey** parancsmag a megadott előfizetés kulcsait kapja meg.</span><span class="sxs-lookup"><span data-stu-id="0f656-106">The **Get-AzApiManagementSubscriptionKey** cmdlet gets a keys of a specified subscription.</span></span>

## <span data-ttu-id="0f656-107">Példák</span><span class="sxs-lookup"><span data-stu-id="0f656-107">EXAMPLES</span></span>

### <span data-ttu-id="0f656-108">Példa 1: előfizetéses kulcsok beszerzése megadott AZONOSÍTÓval</span><span class="sxs-lookup"><span data-stu-id="0f656-108">Example 1: Get a subscription keys with a specified ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-East-US" -ServiceName "contoso"
PS C:\>Get-AzApiManagementSubscriptionKey -Context $apimContext -SubscriptionId "0123456789"

PrimaryKey        : 5e48532634114fe999a6979ce0d63a64
SecondaryKey      : 0a8efaf85a664aa0a412241015c7c8f6
```

<span data-ttu-id="0f656-109">Ez a parancs AZONOSÍTÓval kapja meg az előfizetést.</span><span class="sxs-lookup"><span data-stu-id="0f656-109">This command gets a subscription by ID.</span></span>

## <span data-ttu-id="0f656-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="0f656-110">PARAMETERS</span></span>

### <span data-ttu-id="0f656-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="0f656-111">-Context</span></span>
<span data-ttu-id="0f656-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="0f656-112">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f656-113">-DefaultProfile</span></span>
<span data-ttu-id="0f656-114">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="0f656-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f656-115">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f656-115">-SubscriptionId</span></span>
<span data-ttu-id="0f656-116">Az előfizetés azonosítóját adja meg.</span><span class="sxs-lookup"><span data-stu-id="0f656-116">Specifies a subscription identifier.</span></span>
<span data-ttu-id="0f656-117">Ha meg van adva, ez a parancsmag megkeresi az előfizetést az azonosító alapján.</span><span class="sxs-lookup"><span data-stu-id="0f656-117">If specified, this cmdlet finds subscription by the identifier.</span></span>

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

### <span data-ttu-id="0f656-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f656-118">CommonParameters</span></span>
<span data-ttu-id="0f656-119">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="0f656-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f656-120">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="0f656-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f656-121">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f656-121">INPUTS</span></span>

### <span data-ttu-id="0f656-122">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0f656-122">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0f656-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0f656-123">System.String</span></span>

## <span data-ttu-id="0f656-124">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="0f656-124">OUTPUTS</span></span>

### <span data-ttu-id="0f656-125">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementSubscriptionKey</span><span class="sxs-lookup"><span data-stu-id="0f656-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSubscriptionKey</span></span>

## <span data-ttu-id="0f656-126">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="0f656-126">NOTES</span></span>

## <span data-ttu-id="0f656-127">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="0f656-127">RELATED LINKS</span></span>

[<span data-ttu-id="0f656-128">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0f656-128">New-AzApiManagementSubscription</span></span>](./Get-AzApiManagementSubscription.md)

[<span data-ttu-id="0f656-129">Új – AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0f656-129">New-AzApiManagementSubscription</span></span>](./New-AzApiManagementSubscription.md)

[<span data-ttu-id="0f656-130">Remove-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0f656-130">Remove-AzApiManagementSubscription</span></span>](./Remove-AzApiManagementSubscription.md)

[<span data-ttu-id="0f656-131">Set-AzApiManagementSubscription</span><span class="sxs-lookup"><span data-stu-id="0f656-131">Set-AzApiManagementSubscription</span></span>](./Set-AzApiManagementSubscription.md)


