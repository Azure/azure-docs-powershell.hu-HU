---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: ea18df702913cd2ec7404a3fccb110f85e12ee47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94183765"
---
# <span data-ttu-id="ea8a8-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="ea8a8-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="ea8a8-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="ea8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8a8-103">A PsApiManagementSslSetting példányának létrehozása</span><span class="sxs-lookup"><span data-stu-id="ea8a8-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="ea8a8-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="ea8a8-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ea8a8-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="ea8a8-105">DESCRIPTION</span></span>
<span data-ttu-id="ea8a8-106">A segítő parancs a PsApiManagementSslSetting példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="ea8a8-107">Ezt a parancsot New-AzApiManagement paranccsal kell használni.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="ea8a8-108">Példák</span><span class="sxs-lookup"><span data-stu-id="ea8a8-108">EXAMPLES</span></span>

### <span data-ttu-id="ea8a8-109">1. példa: SSL-beállítás létrehozása, amely lehetővé teszi a TLS 1,0 használatát a Backendeken és a felületeken egyaránt</span><span class="sxs-lookup"><span data-stu-id="ea8a8-109">Example 1: Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="ea8a8-110">A PsApiManagementSslSetting új példányát létrehozhatja a TLSv 1,0-ban mindkét (az ügyfél és a APIM között) és a ApiManagement átjáró (APIM és backend) között.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="ea8a8-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="ea8a8-111">PARAMETERS</span></span>

### <span data-ttu-id="ea8a8-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="ea8a8-112">-BackendProtocol</span></span>
<span data-ttu-id="ea8a8-113">A backend biztonsági protokoll beállításai</span><span class="sxs-lookup"><span data-stu-id="ea8a8-113">Backend Security protocol settings.</span></span> <span data-ttu-id="ea8a8-114">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-114">This parameter is optional.</span></span>
<span data-ttu-id="ea8a8-115">Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="ea8a8-115">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>

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

### <span data-ttu-id="ea8a8-116">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="ea8a8-116">-CipherSuite</span></span>
<span data-ttu-id="ea8a8-117">A megadott sorrendben az SSL-titkosítási lakosztályok beállításai.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-117">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="ea8a8-118">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-118">This parameter is optional.</span></span>
<span data-ttu-id="ea8a8-119">Az érvényes beállítások a `TripleDes168` pacal Des 168-engedélyezése/letiltása</span><span class="sxs-lookup"><span data-stu-id="ea8a8-119">The valid Settings are `TripleDes168` - Enable / Disable Tripe Des 168</span></span>

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

### <span data-ttu-id="ea8a8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea8a8-120">-DefaultProfile</span></span>
<span data-ttu-id="ea8a8-121">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea8a8-122">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="ea8a8-122">-FrontendProtocol</span></span>
<span data-ttu-id="ea8a8-123">Felület biztonsági protokolljainak beállításai</span><span class="sxs-lookup"><span data-stu-id="ea8a8-123">Frontend Security protocols settings.</span></span> <span data-ttu-id="ea8a8-124">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-124">This parameter is optional.</span></span>
<span data-ttu-id="ea8a8-125">Az érvényes protokoll-beállítások a `Tls11` -tls 1,1 `Tls10` -TLS 1,0 `Ssl30` -SSL 3,0</span><span class="sxs-lookup"><span data-stu-id="ea8a8-125">The valid Protocol Settings are `Tls11` - Tls 1.1 `Tls10` - Tls 1.0 `Ssl30` - SSL 3.0</span></span>


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

### <span data-ttu-id="ea8a8-126">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="ea8a8-126">-ServerProtocol</span></span>
<span data-ttu-id="ea8a8-127">A kiszolgálói protokollok beállításai, például a Http2.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-127">Server protocol settings like Http2.</span></span> <span data-ttu-id="ea8a8-128">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-128">This parameter is optional.</span></span>
<span data-ttu-id="ea8a8-129">Az érvényes beállítások engedélyezve vannak a `Http2` http-2,0</span><span class="sxs-lookup"><span data-stu-id="ea8a8-129">The valid Settings are `Http2` - Enable Http 2.0</span></span>

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

### <span data-ttu-id="ea8a8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8a8-130">CommonParameters</span></span>
<span data-ttu-id="ea8a8-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="ea8a8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8a8-132">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="ea8a8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8a8-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea8a8-133">INPUTS</span></span>

### <span data-ttu-id="ea8a8-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="ea8a8-134">None</span></span>

## <span data-ttu-id="ea8a8-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="ea8a8-135">OUTPUTS</span></span>

### <span data-ttu-id="ea8a8-136">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="ea8a8-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="ea8a8-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="ea8a8-137">NOTES</span></span>

## <span data-ttu-id="ea8a8-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="ea8a8-138">RELATED LINKS</span></span>

[<span data-ttu-id="ea8a8-139">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="ea8a8-139">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

