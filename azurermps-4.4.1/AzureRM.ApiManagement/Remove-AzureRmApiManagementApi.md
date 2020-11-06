---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F23D9274-63B9-4654-897B-6E84757774D2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApi.md
ms.openlocfilehash: cadae96af05ae11f76d3a8ea0010da4d73161186
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492613"
---
# <span data-ttu-id="05ee1-101">Remove-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-101">Remove-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="05ee1-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="05ee1-102">SYNOPSIS</span></span>
<span data-ttu-id="05ee1-103">API eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="05ee1-103">Removes an API.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05ee1-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="05ee1-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05ee1-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="05ee1-105">DESCRIPTION</span></span>
<span data-ttu-id="05ee1-106">A **Remove-AzureRmApiManagementApi** parancsmag eltávolítja a meglévő API-t.</span><span class="sxs-lookup"><span data-stu-id="05ee1-106">The **Remove-AzureRmApiManagementApi** cmdlet removes an existing API.</span></span>

## <span data-ttu-id="05ee1-107">Példák</span><span class="sxs-lookup"><span data-stu-id="05ee1-107">EXAMPLES</span></span>

### <span data-ttu-id="05ee1-108">1. példa: API eltávolítása</span><span class="sxs-lookup"><span data-stu-id="05ee1-108">Example 1: Remove an API</span></span>
```
PS C:\>Remove-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789"
```

<span data-ttu-id="05ee1-109">Ez a parancs eltávolítja az API-t a megadott azonosítójú azonosítóval.</span><span class="sxs-lookup"><span data-stu-id="05ee1-109">This command removes the API with the specified ID.</span></span>

## <span data-ttu-id="05ee1-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="05ee1-110">PARAMETERS</span></span>

### <span data-ttu-id="05ee1-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="05ee1-111">-ApiId</span></span>
<span data-ttu-id="05ee1-112">Az API-eltávolítás AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="05ee1-112">Specifies the ID of the API remove.</span></span>

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

### <span data-ttu-id="05ee1-113">-Környezet</span><span class="sxs-lookup"><span data-stu-id="05ee1-113">-Context</span></span>
<span data-ttu-id="05ee1-114">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="05ee1-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="05ee1-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05ee1-115">-PassThru</span></span>
<span data-ttu-id="05ee1-116">passthru</span><span class="sxs-lookup"><span data-stu-id="05ee1-116">passthru</span></span>

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

### <span data-ttu-id="05ee1-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="05ee1-117">-Confirm</span></span>
<span data-ttu-id="05ee1-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="05ee1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05ee1-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ee1-119">-WhatIf</span></span>
<span data-ttu-id="05ee1-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="05ee1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ee1-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="05ee1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05ee1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ee1-122">-DefaultProfile</span></span>
<span data-ttu-id="05ee1-123">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="05ee1-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05ee1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ee1-124">CommonParameters</span></span>
<span data-ttu-id="05ee1-125">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="05ee1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ee1-126">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05ee1-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ee1-127">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="05ee1-127">INPUTS</span></span>

## <span data-ttu-id="05ee1-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="05ee1-128">OUTPUTS</span></span>

### <span data-ttu-id="05ee1-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="05ee1-129">Boolean</span></span>

## <span data-ttu-id="05ee1-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="05ee1-130">NOTES</span></span>

## <span data-ttu-id="05ee1-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="05ee1-131">RELATED LINKS</span></span>

[<span data-ttu-id="05ee1-132">Exportálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-132">Export-AzureRmApiManagementApi</span></span>](./Export-AzureRmApiManagementApi.md)

[<span data-ttu-id="05ee1-133">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-133">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="05ee1-134">Importálás – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-134">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="05ee1-135">Új – AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-135">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="05ee1-136">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="05ee1-136">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


