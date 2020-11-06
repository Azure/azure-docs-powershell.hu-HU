---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementAuthorizationServer.md
ms.openlocfilehash: 2fc658f5bab9e6233e6b7279abc0ae80832bcc8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492078"
---
# <span data-ttu-id="ea059-101">Remove-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea059-101">Remove-AzureRmApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="ea059-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea059-102">SYNOPSIS</span></span>
<span data-ttu-id="ea059-103">Egy engedélyezési kiszolgáló eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="ea059-103">Removes an authorization server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea059-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea059-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea059-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea059-105">DESCRIPTION</span></span>
<span data-ttu-id="ea059-106">A **Remove-AzureRmApiManagementAuthorizationServer** parancsmag eltávolítja az Azure API-kezelési engedélyezési kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="ea059-106">The **Remove-AzureRmApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="ea059-107">Példák</span><span class="sxs-lookup"><span data-stu-id="ea059-107">EXAMPLES</span></span>

## <span data-ttu-id="ea059-108">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea059-108">PARAMETERS</span></span>

### <span data-ttu-id="ea059-109">-Környezet</span><span class="sxs-lookup"><span data-stu-id="ea059-109">-Context</span></span>
<span data-ttu-id="ea059-110">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="ea059-110">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="ea059-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea059-111">-DefaultProfile</span></span>
<span data-ttu-id="ea059-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea059-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea059-113">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea059-113">-PassThru</span></span>
<span data-ttu-id="ea059-114">passthru</span><span class="sxs-lookup"><span data-stu-id="ea059-114">passthru</span></span>

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

### <span data-ttu-id="ea059-115">-ServerId</span><span class="sxs-lookup"><span data-stu-id="ea059-115">-ServerId</span></span>
<span data-ttu-id="ea059-116">Az eltávolítandó engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="ea059-116">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="ea059-117">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="ea059-117">-Confirm</span></span>
<span data-ttu-id="ea059-118">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="ea059-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea059-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea059-119">-WhatIf</span></span>
<span data-ttu-id="ea059-120">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="ea059-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea059-121">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="ea059-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea059-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea059-122">CommonParameters</span></span>
<span data-ttu-id="ea059-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea059-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea059-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea059-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea059-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea059-125">INPUTS</span></span>

### <span data-ttu-id="ea059-126">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ea059-126">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ea059-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ea059-127">System.String</span></span>

### <span data-ttu-id="ea059-128">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ea059-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ea059-129">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea059-129">OUTPUTS</span></span>

### <span data-ttu-id="ea059-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea059-130">System.Boolean</span></span>

## <span data-ttu-id="ea059-131">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea059-131">NOTES</span></span>

## <span data-ttu-id="ea059-132">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea059-132">RELATED LINKS</span></span>

[<span data-ttu-id="ea059-133">Get-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea059-133">Get-AzureRmApiManagementAuthorizationServer</span></span>](./Get-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ea059-134">Új – AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea059-134">New-AzureRmApiManagementAuthorizationServer</span></span>](./New-AzureRmApiManagementAuthorizationServer.md)

[<span data-ttu-id="ea059-135">Set-AzureRmApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="ea059-135">Set-AzureRmApiManagementAuthorizationServer</span></span>](./Set-AzureRmApiManagementAuthorizationServer.md)


