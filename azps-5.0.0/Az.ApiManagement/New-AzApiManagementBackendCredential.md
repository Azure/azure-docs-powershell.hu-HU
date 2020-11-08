---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendCredential.md
ms.openlocfilehash: 069bf57b62d6834a1509adb551d15ce5082b2dc3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186284"
---
# <span data-ttu-id="b95da-101">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b95da-101">New-AzApiManagementBackendCredential</span></span>

## <span data-ttu-id="b95da-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="b95da-102">SYNOPSIS</span></span>
<span data-ttu-id="b95da-103">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="b95da-103">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b95da-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="b95da-104">SYNTAX</span></span>

```
New-AzApiManagementBackendCredential [-CertificateThumbprint <String[]>] [-Query <Hashtable>]
 [-Header <Hashtable>] [-AuthorizationHeaderScheme <String>] [-AuthorizationHeaderParameter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b95da-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="b95da-105">DESCRIPTION</span></span>
<span data-ttu-id="b95da-106">Létrehoz egy új backend hitelesítő adatokat tartalmazó szerződést.</span><span class="sxs-lookup"><span data-stu-id="b95da-106">Creates a new Backend Credential contract.</span></span>

## <span data-ttu-id="b95da-107">Példák</span><span class="sxs-lookup"><span data-stu-id="b95da-107">EXAMPLES</span></span>

### <span data-ttu-id="b95da-108">Példa 1: backend-hitelesítő adatok létrehozása In-Memory objektummal</span><span class="sxs-lookup"><span data-stu-id="b95da-108">Example 1: Create a Backend Credentials In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b95da-109">A backend-hitelesítő adatokkal rendelkező szerződés létrehozása</span><span class="sxs-lookup"><span data-stu-id="b95da-109">Creates a Backend Credentials Contract</span></span>

## <span data-ttu-id="b95da-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="b95da-110">PARAMETERS</span></span>

### <span data-ttu-id="b95da-111">-AuthorizationHeaderParameter</span><span class="sxs-lookup"><span data-stu-id="b95da-111">-AuthorizationHeaderParameter</span></span>
<span data-ttu-id="b95da-112">A backendhez használt engedélyezési fejléc.</span><span class="sxs-lookup"><span data-stu-id="b95da-112">Authorization Header used for the Backend.</span></span>
<span data-ttu-id="b95da-113">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b95da-113">This parameter is optional.</span></span>

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

### <span data-ttu-id="b95da-114">-AuthorizationHeaderScheme</span><span class="sxs-lookup"><span data-stu-id="b95da-114">-AuthorizationHeaderScheme</span></span>
<span data-ttu-id="b95da-115">A backendhez használt engedélyezési séma.</span><span class="sxs-lookup"><span data-stu-id="b95da-115">Authorization Scheme used for the Backend.</span></span>
<span data-ttu-id="b95da-116">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b95da-116">This parameter is optional.</span></span>

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

### <span data-ttu-id="b95da-117">-CertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="b95da-117">-CertificateThumbprint</span></span>
<span data-ttu-id="b95da-118">Ügyféltanúsítvány-Thumbprints</span><span class="sxs-lookup"><span data-stu-id="b95da-118">Client Certificate Thumbprints.</span></span>
<span data-ttu-id="b95da-119">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b95da-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="b95da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b95da-120">-DefaultProfile</span></span>
<span data-ttu-id="b95da-121">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="b95da-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b95da-122">-Header</span><span class="sxs-lookup"><span data-stu-id="b95da-122">-Header</span></span>
<span data-ttu-id="b95da-123">A backend által elfogadott fejléc paraméter-értékek</span><span class="sxs-lookup"><span data-stu-id="b95da-123">Header Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b95da-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b95da-124">This parameter is optional.</span></span>

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

### <span data-ttu-id="b95da-125">-Query</span><span class="sxs-lookup"><span data-stu-id="b95da-125">-Query</span></span>
<span data-ttu-id="b95da-126">A lekérdezés paramétereit a backend által elfogadott értékekkel.</span><span class="sxs-lookup"><span data-stu-id="b95da-126">Query Parameter Values accepted by Backend.</span></span>
<span data-ttu-id="b95da-127">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="b95da-127">This parameter is optional.</span></span>

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

### <span data-ttu-id="b95da-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b95da-128">CommonParameters</span></span>
<span data-ttu-id="b95da-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="b95da-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b95da-130">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="b95da-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b95da-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="b95da-131">INPUTS</span></span>

### <span data-ttu-id="b95da-132">Nincs</span><span class="sxs-lookup"><span data-stu-id="b95da-132">None</span></span>

## <span data-ttu-id="b95da-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="b95da-133">OUTPUTS</span></span>

### <span data-ttu-id="b95da-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b95da-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

## <span data-ttu-id="b95da-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="b95da-135">NOTES</span></span>

## <span data-ttu-id="b95da-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="b95da-136">RELATED LINKS</span></span>

[<span data-ttu-id="b95da-137">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b95da-137">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b95da-138">Új – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b95da-138">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="b95da-139">Új – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b95da-139">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b95da-140">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b95da-140">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b95da-141">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b95da-141">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
