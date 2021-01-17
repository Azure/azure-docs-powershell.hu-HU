---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: C2CC10DE-1D36-4937-8A3E-9776BE80DF9A
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementauthorizationserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementAuthorizationServer.md
ms.openlocfilehash: 74e876621948587c116f435f70315c04b403c2f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382156"
---
# <span data-ttu-id="19911-101">Remove-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19911-101">Remove-AzApiManagementAuthorizationServer</span></span>

## <span data-ttu-id="19911-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19911-102">SYNOPSIS</span></span>
<span data-ttu-id="19911-103">Eltávolít egy engedélyezési kiszolgálót.</span><span class="sxs-lookup"><span data-stu-id="19911-103">Removes an authorization server.</span></span>

## <span data-ttu-id="19911-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="19911-104">SYNTAX</span></span>

```
Remove-AzApiManagementAuthorizationServer -Context <PsApiManagementContext> -ServerId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19911-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="19911-105">DESCRIPTION</span></span>
<span data-ttu-id="19911-106">A **Remove-AzApiManagementAuthorizationServer** parancsmag eltávolítja az Azure API Management engedélyezési kiszolgálóját.</span><span class="sxs-lookup"><span data-stu-id="19911-106">The **Remove-AzApiManagementAuthorizationServer** cmdlet removes an Azure API Management authorization server.</span></span>

## <span data-ttu-id="19911-107">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="19911-107">EXAMPLES</span></span>

### <span data-ttu-id="19911-108">1. példa: Engedélyezési kiszolgáló eltávolítása</span><span class="sxs-lookup"><span data-stu-id="19911-108">Example 1: Remove an authorization server</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementAuthorizationServer -Context $ApiMgmtContext -ServerId "authserverid" -Force
```

<span data-ttu-id="19911-109">Ez a parancs eltávolítja a megadott API Management Authorization Servert.</span><span class="sxs-lookup"><span data-stu-id="19911-109">This command removes the specified API Management Authorization Server.</span></span>
<span data-ttu-id="19911-110">Mivel a *Force paraméter* meg van adva, nincs szükség megerősítésre.</span><span class="sxs-lookup"><span data-stu-id="19911-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="19911-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19911-111">PARAMETERS</span></span>

### <span data-ttu-id="19911-112">-Környezet</span><span class="sxs-lookup"><span data-stu-id="19911-112">-Context</span></span>
<span data-ttu-id="19911-113">Egy **PsApiManagementContext objektumot** ad meg.</span><span class="sxs-lookup"><span data-stu-id="19911-113">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="19911-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19911-114">-DefaultProfile</span></span>
<span data-ttu-id="19911-115">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="19911-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19911-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19911-116">-PassThru</span></span>
<span data-ttu-id="19911-117">passthru</span><span class="sxs-lookup"><span data-stu-id="19911-117">passthru</span></span>

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

### <span data-ttu-id="19911-118">-ServerId</span><span class="sxs-lookup"><span data-stu-id="19911-118">-ServerId</span></span>
<span data-ttu-id="19911-119">Az eltávolítható engedélyezési kiszolgáló azonosítója.</span><span class="sxs-lookup"><span data-stu-id="19911-119">Specifies the ID of the authorization server to remove.</span></span>

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

### <span data-ttu-id="19911-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19911-120">-Confirm</span></span>
<span data-ttu-id="19911-121">A parancsmag futtatása előtt a rendszer megerősítést kér.</span><span class="sxs-lookup"><span data-stu-id="19911-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19911-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19911-122">-WhatIf</span></span>
<span data-ttu-id="19911-123">A parancsmag futtatásakor a program megjeleníti, hogy mi történik.</span><span class="sxs-lookup"><span data-stu-id="19911-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19911-124">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="19911-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19911-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19911-125">CommonParameters</span></span>
<span data-ttu-id="19911-126">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19911-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19911-127">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="19911-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19911-128">INPUTS</span><span class="sxs-lookup"><span data-stu-id="19911-128">INPUTS</span></span>

### <span data-ttu-id="19911-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="19911-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="19911-130">System.String</span><span class="sxs-lookup"><span data-stu-id="19911-130">System.String</span></span>

### <span data-ttu-id="19911-131">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="19911-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="19911-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="19911-132">OUTPUTS</span></span>

### <span data-ttu-id="19911-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="19911-133">System.Boolean</span></span>

## <span data-ttu-id="19911-134">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="19911-134">NOTES</span></span>

## <span data-ttu-id="19911-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="19911-135">RELATED LINKS</span></span>

[<span data-ttu-id="19911-136">Get-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19911-136">Get-AzApiManagementAuthorizationServer</span></span>](./Get-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="19911-137">New-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19911-137">New-AzApiManagementAuthorizationServer</span></span>](./New-AzApiManagementAuthorizationServer.md)

[<span data-ttu-id="19911-138">Set-AzApiManagementAuthorizationServer</span><span class="sxs-lookup"><span data-stu-id="19911-138">Set-AzApiManagementAuthorizationServer</span></span>](./Set-AzApiManagementAuthorizationServer.md)


