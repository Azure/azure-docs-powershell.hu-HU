---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: c9133c7a2924b4151afd01f257fe6b54a9eeb00d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504631"
---
# <span data-ttu-id="15534-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="15534-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="15534-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15534-102">SYNOPSIS</span></span>
<span data-ttu-id="15534-103">Egy engedélyezési kiszolgáló eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="15534-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="15534-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15534-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15534-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15534-105">DESCRIPTION</span></span>
<span data-ttu-id="15534-106">A **Remove-AzureRmApiManagementAuthorizationServer** parancsmag eltávolítja az Azure API-kezelési engedélyezési kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="15534-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="15534-107">Példák</span><span class="sxs-lookup"><span data-stu-id="15534-107">EXAMPLES</span></span>

## <span data-ttu-id="15534-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15534-108">PARAMETERS</span></span>

### <span data-ttu-id="15534-109">-Környezet</span><span class="sxs-lookup"><span data-stu-id="15534-109">-Context</span></span>
<span data-ttu-id="15534-110">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="15534-110">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15534-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15534-111">-DefaultProfile</span></span>
<span data-ttu-id="15534-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15534-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="15534-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15534-113">-PassThru</span></span>
<span data-ttu-id="15534-114">passthru</span><span class="sxs-lookup"><span data-stu-id="15534-114">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15534-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="15534-115">-ServerId</span></span>
<span data-ttu-id="15534-116">Az eltávolítandó engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15534-116">Specifies the ID of the authorization server to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15534-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15534-117">-Confirm</span></span>
<span data-ttu-id="15534-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15534-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15534-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15534-119">-WhatIf</span></span>
<span data-ttu-id="15534-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15534-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15534-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15534-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15534-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15534-122">CommonParameters</span></span>
<span data-ttu-id="15534-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15534-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15534-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15534-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15534-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15534-125">INPUTS</span></span>

### <span data-ttu-id="15534-126">Nincs</span><span class="sxs-lookup"><span data-stu-id="15534-126">None</span></span>
<span data-ttu-id="15534-127">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="15534-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="15534-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15534-128">OUTPUTS</span></span>

### <span data-ttu-id="15534-129">Logikai</span><span class="sxs-lookup"><span data-stu-id="15534-129">Boolean</span></span>

## <span data-ttu-id="15534-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15534-130">NOTES</span></span>

## <span data-ttu-id="15534-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15534-131">RELATED LINKS</span></span>

[<span data-ttu-id="15534-132">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="15534-132">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="15534-133">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="15534-133">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="15534-134">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="15534-134">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


