---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299876"
---
# <span data-ttu-id="670fc-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="670fc-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="670fc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="670fc-102">SYNOPSIS</span></span>
<span data-ttu-id="670fc-103">Egy engedélyezési kiszolgáló eltávolítása.</span><span class="sxs-lookup"><span data-stu-id="670fc-103">Removes an authorization server.</span></span>

## <span data-ttu-id="670fc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="670fc-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="670fc-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="670fc-105">DESCRIPTION</span></span>
<span data-ttu-id="670fc-106">A **Remove-AzApiManagementAuthorizationServer** parancsmag eltávolítja az Azure API-kezelési engedélyezési kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="670fc-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="670fc-107">Példák</span><span class="sxs-lookup"><span data-stu-id="670fc-107">EXAMPLES</span></span>

### <span data-ttu-id="670fc-108">1. példa: engedélyezési kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="670fc-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="670fc-109">Ez a parancs eltávolítja a megadott API-kezelési engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="670fc-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="670fc-110">Mivel az *erő* paraméter van megadva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="670fc-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="670fc-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="670fc-111">PARAMETERS</span></span>

### <span data-ttu-id="670fc-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="670fc-112">-Context</span></span>
<span data-ttu-id="670fc-113">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="670fc-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="670fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="670fc-114">-DefaultProfile</span></span>
<span data-ttu-id="670fc-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="670fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="670fc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="670fc-116">-PassThru</span></span>
<span data-ttu-id="670fc-117">passthru</span><span class="sxs-lookup"><span data-stu-id="670fc-117">passthru</span></span>

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

### <span data-ttu-id="670fc-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="670fc-118">-ServerId</span></span>
<span data-ttu-id="670fc-119">Az eltávolítandó engedélyezési kiszolgáló AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="670fc-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="670fc-120">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="670fc-120">-Confirm</span></span>
<span data-ttu-id="670fc-121">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="670fc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="670fc-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="670fc-122">-WhatIf</span></span>
<span data-ttu-id="670fc-123">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="670fc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="670fc-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="670fc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="670fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="670fc-125">CommonParameters</span></span>
<span data-ttu-id="670fc-126">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="670fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="670fc-127">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="670fc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="670fc-128">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="670fc-128">INPUTS</span></span>

### <span data-ttu-id="670fc-129">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="670fc-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="670fc-130">System. String</span><span class="sxs-lookup"><span data-stu-id="670fc-130">System.String</span></span>

### <span data-ttu-id="670fc-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="670fc-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="670fc-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="670fc-132">OUTPUTS</span></span>

### <span data-ttu-id="670fc-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="670fc-133">System.Boolean</span></span>

## <span data-ttu-id="670fc-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="670fc-134">NOTES</span></span>

## <span data-ttu-id="670fc-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="670fc-135">RELATED LINKS</span></span>

[<span data-ttu-id="670fc-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="670fc-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="670fc-137">Új – AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="670fc-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="670fc-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="670fc-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


