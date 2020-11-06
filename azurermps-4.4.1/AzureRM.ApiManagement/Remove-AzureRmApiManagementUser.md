---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 441BC2EE-DBB7-4579-BA64-9D3042B7EBD8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementUser.md
ms.openlocfilehash: 6be4c714627d77b0e3c56b8dd9766c550deebd7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492592"
---
# <span data-ttu-id="40e6a-101">Remove-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40e6a-101">Remove-AzureRmApiManagementUser</span></span>

## <span data-ttu-id="40e6a-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="40e6a-103">Egy meglévő felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="40e6a-103">Deletes an existing user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40e6a-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40e6a-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementUser -Context <PsApiManagementContext> -UserId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40e6a-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40e6a-105">DESCRIPTION</span></span>
<span data-ttu-id="40e6a-106">A **Remove-AzureRmApiManagementUser** parancsmag egy meglévő felhasználó törlésére.</span><span class="sxs-lookup"><span data-stu-id="40e6a-106">The **Remove-AzureRmApiManagementUser** cmdlet deletes an existing user.</span></span>

## <span data-ttu-id="40e6a-107">Példák</span><span class="sxs-lookup"><span data-stu-id="40e6a-107">EXAMPLES</span></span>

### <span data-ttu-id="40e6a-108">Példa 1: felhasználó törlése</span><span class="sxs-lookup"><span data-stu-id="40e6a-108">Example 1: Delete a user</span></span>
```
PS C:\>Remove-AzureRmApiManagementUser -Context $apimContext -UserId "0123456789" -Force
```

<span data-ttu-id="40e6a-109">Ez a parancs egy meglévő felhasználót töröl.</span><span class="sxs-lookup"><span data-stu-id="40e6a-109">This command deletes an existing user.</span></span>

## <span data-ttu-id="40e6a-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40e6a-110">PARAMETERS</span></span>

### <span data-ttu-id="40e6a-111">-Környezet</span><span class="sxs-lookup"><span data-stu-id="40e6a-111">-Context</span></span>
<span data-ttu-id="40e6a-112">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="40e6a-112">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="40e6a-113">Ehhez a paraméterhez szükség van.</span><span class="sxs-lookup"><span data-stu-id="40e6a-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-114">-DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="40e6a-114">-DeleteSubscriptions</span></span>
<span data-ttu-id="40e6a-115">Azt jelzi, hogy törli-e az előfizetéseket a terméket.</span><span class="sxs-lookup"><span data-stu-id="40e6a-115">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="40e6a-116">Ha ez a paraméter nincs megadva, és létezik egy előfizetés, ez a parancsmag kivételt okoz.</span><span class="sxs-lookup"><span data-stu-id="40e6a-116">If this parameter is not specified and a subscription exists, this cmdlet throws an exception.</span></span>
<span data-ttu-id="40e6a-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="40e6a-117">This parameter is optional.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40e6a-118">-PassThru</span></span>
<span data-ttu-id="40e6a-119">Azt jelzi, hogy ez a parancsmag az $Ture értékét adja eredményül, ha a művelet sikeres, vagy ha az $False értéke más.</span><span class="sxs-lookup"><span data-stu-id="40e6a-119">Indicates that this cmdlet returns a value of $Ture, if it succeeds, or a value of $False, otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-120">-UserId</span><span class="sxs-lookup"><span data-stu-id="40e6a-120">-UserId</span></span>
<span data-ttu-id="40e6a-121">Megadja az eltávolítandó felhasználó AZONOSÍTÓját.</span><span class="sxs-lookup"><span data-stu-id="40e6a-121">Specifies the ID of the user to remove.</span></span>

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

### <span data-ttu-id="40e6a-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="40e6a-122">-Confirm</span></span>
<span data-ttu-id="40e6a-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="40e6a-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40e6a-124">-WhatIf</span></span>
<span data-ttu-id="40e6a-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="40e6a-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40e6a-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="40e6a-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40e6a-127">-DefaultProfile</span></span>
<span data-ttu-id="40e6a-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40e6a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40e6a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40e6a-129">CommonParameters</span></span>
<span data-ttu-id="40e6a-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40e6a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40e6a-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40e6a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40e6a-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e6a-132">INPUTS</span></span>

## <span data-ttu-id="40e6a-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40e6a-133">OUTPUTS</span></span>

### <span data-ttu-id="40e6a-134">Logikai</span><span class="sxs-lookup"><span data-stu-id="40e6a-134">Boolean</span></span>

## <span data-ttu-id="40e6a-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40e6a-135">NOTES</span></span>

## <span data-ttu-id="40e6a-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40e6a-136">RELATED LINKS</span></span>

[<span data-ttu-id="40e6a-137">Get-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40e6a-137">Get-AzureRmApiManagementUser</span></span>](./Get-AzureRmApiManagementUser.md)

[<span data-ttu-id="40e6a-138">Új – AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40e6a-138">New-AzureRmApiManagementUser</span></span>](./New-AzureRmApiManagementUser.md)

[<span data-ttu-id="40e6a-139">Set-AzureRmApiManagementUser</span><span class="sxs-lookup"><span data-stu-id="40e6a-139">Set-AzureRmApiManagementUser</span></span>](./Set-AzureRmApiManagementUser.md)


