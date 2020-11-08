---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 709e8483a5f21e3afc58add1046b5dae22bea7b8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94012209"
---
# <span data-ttu-id="20250-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="20250-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="20250-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="20250-102">SYNOPSIS</span></span>
<span data-ttu-id="20250-103">A PsApiManagementSslSetting példányának létrehozása</span><span class="sxs-lookup"><span data-stu-id="20250-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="20250-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="20250-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20250-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="20250-105">DESCRIPTION</span></span>
<span data-ttu-id="20250-106">A segítő parancs a PsApiManagementSslSetting példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="20250-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="20250-107">Ezt a parancsot New-AzApiManagement paranccsal kell használni.</span><span class="sxs-lookup"><span data-stu-id="20250-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="20250-108">Példák</span><span class="sxs-lookup"><span data-stu-id="20250-108">EXAMPLES</span></span>

### <span data-ttu-id="20250-109">1. példa: SSL-beállítás létrehozása, amely lehetővé teszi a TLS 1,0 használatát a Backendeken és a felületeken egyaránt</span><span class="sxs-lookup"><span data-stu-id="20250-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="20250-110">A PsApiManagementSslSetting új példányát létrehozhatja a TLSv 1,0-ban mindkét (az ügyfél és a APIM között) és a ApiManagement átjáró (APIM és backend) között.</span><span class="sxs-lookup"><span data-stu-id="20250-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="20250-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="20250-111">PARAMETERS</span></span>

### <span data-ttu-id="20250-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="20250-112">-BackendProtocol</span></span>
<span data-ttu-id="20250-113">A backend biztonsági protokoll beállításai</span><span class="sxs-lookup"><span data-stu-id="20250-113">Backend Security protocol settings.</span></span> <span data-ttu-id="20250-114">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20250-114">This parameter is optional.</span></span>
<span data-ttu-id="20250-115">Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="20250-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="20250-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="20250-116">-CipherSuite</span></span>
<span data-ttu-id="20250-117">A megadott sorrendben az SSL-titkosítási lakosztályok beállításai.</span><span class="sxs-lookup"><span data-stu-id="20250-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="20250-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20250-118">This parameter is optional.</span></span>
<span data-ttu-id="20250-119">Az érvényes beállítások a `TripleDes168` pacal Des 168-engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="20250-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="20250-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20250-120">-DefaultProfile</span></span>
<span data-ttu-id="20250-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="20250-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20250-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="20250-122">-FrontendProtocol</span></span>
<span data-ttu-id="20250-123">Felület biztonsági protokolljainak beállításai</span><span class="sxs-lookup"><span data-stu-id="20250-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="20250-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20250-124">This parameter is optional.</span></span>
<span data-ttu-id="20250-125">Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="20250-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="20250-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="20250-126">-ServerProtocol</span></span>
<span data-ttu-id="20250-127">A kiszolgálói protokollok beállításai, például a Http2.</span><span class="sxs-lookup"><span data-stu-id="20250-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="20250-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="20250-128">This parameter is optional.</span></span>
<span data-ttu-id="20250-129">Az érvényes beállítások engedélyezve vannak a `Http2` http-2,0</span><span class="sxs-lookup"><span data-stu-id="20250-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="20250-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20250-130">CommonParameters</span></span>
<span data-ttu-id="20250-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="20250-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20250-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="20250-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20250-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="20250-133">INPUTS</span></span>

### <span data-ttu-id="20250-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="20250-134">None</span></span>

## <span data-ttu-id="20250-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="20250-135">OUTPUTS</span></span>

### <span data-ttu-id="20250-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="20250-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="20250-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="20250-137">NOTES</span></span>

## <span data-ttu-id="20250-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="20250-138">RELATED LINKS</span></span>

[<span data-ttu-id="20250-139">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="20250-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

