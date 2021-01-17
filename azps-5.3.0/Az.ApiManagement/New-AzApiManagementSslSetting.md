---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382407"
---
# <span data-ttu-id="5df3a-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="5df3a-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="5df3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5df3a-102">SYNOPSIS</span></span>
<span data-ttu-id="5df3a-103">Létrehozza a PsApiManagementSslSetting egy példányát</span><span class="sxs-lookup"><span data-stu-id="5df3a-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="5df3a-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="5df3a-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5df3a-105">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="5df3a-105">DESCRIPTION</span></span>
<span data-ttu-id="5df3a-106">Helper command to create an instance of PsApiManagementSslSetting.</span><span class="sxs-lookup"><span data-stu-id="5df3a-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="5df3a-107">Ez a parancs a New-AzApiManagement használható.</span><span class="sxs-lookup"><span data-stu-id="5df3a-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="5df3a-108">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="5df3a-108">EXAMPLES</span></span>

### <span data-ttu-id="5df3a-109">1. példa: SSL-beállítás létrehozása a TLS 1.0 engedélyezéséhez Backend és Frontend esetén is</span><span class="sxs-lookup"><span data-stu-id="5df3a-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="5df3a-110">Hozzon létre egy új PsApiManagementSslSetting példányt az ApiManagement Gateway Előtűnés (ügyfél és APIM között) és Backend (APIM és Backend között) előtűnésében (az APIM és a Backend között) való engedélyezéséhez.</span><span class="sxs-lookup"><span data-stu-id="5df3a-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="5df3a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5df3a-111">PARAMETERS</span></span>

### <span data-ttu-id="5df3a-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="5df3a-112">-BackendProtocol</span></span>
<span data-ttu-id="5df3a-113">Backend Security protocol settings.</span><span class="sxs-lookup"><span data-stu-id="5df3a-113">Backend Security protocol settings.</span></span> <span data-ttu-id="5df3a-114">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5df3a-114">This parameter is optional.</span></span>
<span data-ttu-id="5df3a-115">Az érvényes protokollbeállítások `Tls11` : - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="5df3a-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="5df3a-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="5df3a-116">-CipherSuite</span></span>
<span data-ttu-id="5df3a-117">Ssl cipher suites settings in the specified order.</span><span class="sxs-lookup"><span data-stu-id="5df3a-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="5df3a-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5df3a-118">This parameter is optional.</span></span>
<span data-ttu-id="5df3a-119">Az érvényes beállítások a `TripleDes168` következők: – Tripe Des 168 engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="5df3a-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="5df3a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5df3a-120">-DefaultProfile</span></span>
<span data-ttu-id="5df3a-121">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="5df3a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5df3a-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="5df3a-122">-FrontendProtocol</span></span>
<span data-ttu-id="5df3a-123">Frontend Security protocols settings.</span><span class="sxs-lookup"><span data-stu-id="5df3a-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="5df3a-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5df3a-124">This parameter is optional.</span></span>
<span data-ttu-id="5df3a-125">Az érvényes protokollbeállítások `Tls11` : - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span><span class="sxs-lookup"><span data-stu-id="5df3a-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="5df3a-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="5df3a-126">-ServerProtocol</span></span>
<span data-ttu-id="5df3a-127">Kiszolgálói protokollbeállítások, például Http2.</span><span class="sxs-lookup"><span data-stu-id="5df3a-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="5df3a-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="5df3a-128">This parameter is optional.</span></span>
<span data-ttu-id="5df3a-129">Az érvényes beállítások : `Http2` Http 2.0 engedélyezése</span><span class="sxs-lookup"><span data-stu-id="5df3a-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="5df3a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5df3a-130">CommonParameters</span></span>
<span data-ttu-id="5df3a-131">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5df3a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5df3a-132">További információt a [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5df3a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5df3a-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5df3a-133">INPUTS</span></span>

### <span data-ttu-id="5df3a-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="5df3a-134">None</span></span>

## <span data-ttu-id="5df3a-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="5df3a-135">OUTPUTS</span></span>

### <span data-ttu-id="5df3a-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="5df3a-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="5df3a-137">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="5df3a-137">NOTES</span></span>

## <span data-ttu-id="5df3a-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="5df3a-138">RELATED LINKS</span></span>

[<span data-ttu-id="5df3a-139">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="5df3a-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

