---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 2cde898622c870dc0598639addb1e8b30e438076
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668061"
---
# <span data-ttu-id="9d285-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9d285-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="9d285-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9d285-102">SYNOPSIS</span></span>
<span data-ttu-id="9d285-103">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="9d285-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="9d285-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9d285-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d285-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="9d285-105">DESCRIPTION</span></span>
<span data-ttu-id="9d285-106">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="9d285-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="9d285-107">Példák</span><span class="sxs-lookup"><span data-stu-id="9d285-107">EXAMPLES</span></span>

### <span data-ttu-id="9d285-108">Backend-hitelesítő adatok In-Memory objektum létrehozása</span><span class="sxs-lookup"><span data-stu-id="9d285-108">Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="9d285-109">A backend-hitelesítő adatokkal rendelkező szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="9d285-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="9d285-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9d285-110">PARAMETERS</span></span>

### <span data-ttu-id="9d285-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="9d285-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="9d285-112">A backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="9d285-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="9d285-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9d285-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d285-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="9d285-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="9d285-115">A backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="9d285-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="9d285-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9d285-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d285-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="9d285-117">-CertificateThumbprint</span></span>
<span data-ttu-id="9d285-118">Ügyféltanúsítvány-Thumbprints</span><span class="sxs-lookup"><span data-stu-id="9d285-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="9d285-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9d285-119">This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d285-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d285-120">-DefaultProfile</span></span>
<span data-ttu-id="9d285-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9d285-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d285-122">-Header</span><span class="sxs-lookup"><span data-stu-id="9d285-122">-Header</span></span>
<span data-ttu-id="9d285-123">A backend által elfogadott fejléc paraméter-értékek</span><span class="sxs-lookup"><span data-stu-id="9d285-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="9d285-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9d285-124">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d285-125">-Query</span><span class="sxs-lookup"><span data-stu-id="9d285-125">-Query</span></span>
<span data-ttu-id="9d285-126">A lekérdezés paramétereit a backend által elfogadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="9d285-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="9d285-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="9d285-127">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d285-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d285-128">CommonParameters</span></span>
<span data-ttu-id="9d285-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9d285-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d285-130">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="9d285-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d285-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d285-131">INPUTS</span></span>

### <span data-ttu-id="9d285-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="9d285-132">None</span></span>

## <span data-ttu-id="9d285-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9d285-133">OUTPUTS</span></span>

### <span data-ttu-id="9d285-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="9d285-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="9d285-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9d285-135">NOTES</span></span>

## <span data-ttu-id="9d285-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9d285-136">RELATED LINKS</span></span>

[<span data-ttu-id="9d285-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d285-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="9d285-138">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d285-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="9d285-139">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="9d285-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="9d285-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d285-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="9d285-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="9d285-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
