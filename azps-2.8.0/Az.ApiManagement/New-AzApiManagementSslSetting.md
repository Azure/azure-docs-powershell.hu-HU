---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsslsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSslSetting.md
ms.openlocfilehash: 7c4fb7c2147d7daf3307c2895893198ebe805ff0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93668023"
---
# <span data-ttu-id="382ce-101">New-AzApiManagementSslSetting</span><span class="sxs-lookup"><span data-stu-id="382ce-101">New-AzApiManagementSslSetting</span></span>

## <span data-ttu-id="382ce-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="382ce-102">SYNOPSIS</span></span>
<span data-ttu-id="382ce-103">A PsApiManagementSslSetting példányának létrehozása</span><span class="sxs-lookup"><span data-stu-id="382ce-103">Creates an instance of PsApiManagementSslSetting</span></span>

## <span data-ttu-id="382ce-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="382ce-104">SYNTAX</span></span>

```
New-AzApiManagementSslSetting [-FrontendProtocol <Hashtable>] [-BackendProtocol <Hashtable>]
 [-CipherSuite <Hashtable>] [-ServerProtocol <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="382ce-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="382ce-105">DESCRIPTION</span></span>
<span data-ttu-id="382ce-106">A segítő parancs a PsApiManagementSslSetting példányának létrehozásához.</span><span class="sxs-lookup"><span data-stu-id="382ce-106">Helper command to create an instance of PsApiManagementSslSetting.</span></span>
<span data-ttu-id="382ce-107">Ezt a parancsot New-AzApiManagement paranccsal kell használni.</span><span class="sxs-lookup"><span data-stu-id="382ce-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="382ce-108">Példák</span><span class="sxs-lookup"><span data-stu-id="382ce-108">EXAMPLES</span></span>

### <span data-ttu-id="382ce-109">1. példa: SSL-beállítás létrehozása, amely lehetővé teszi a TLS 1,0 használatát a Backendeken és a felületeken egyaránt</span><span class="sxs-lookup"><span data-stu-id="382ce-109">Example 1 : Create an SSL Setting to enable TLS 1.0 on both Backend and Frontend</span></span>
```powershell
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> $enableTls=@{"Tls10" = "True"}
PS D:\github\azure-powershell\artifacts\Debug\Az.ApiManagement> New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls

FrontendProtocols BackendProtocols CipherSuites ServerProtocols
----------------- ---------------- ------------ ---------------
{Tls10}           {Tls10}
```

<span data-ttu-id="382ce-110">A PsApiManagementSslSetting új példányát létrehozhatja a TLSv 1,0-ban mindkét (az ügyfél és a APIM között) és a ApiManagement átjáró (APIM és backend) között.</span><span class="sxs-lookup"><span data-stu-id="382ce-110">Create an new instance of PsApiManagementSslSetting to Enable TLSv 1.0 in both Frontend (between client and APIM) and Backend (between APIM and Backend) of ApiManagement Gateway.</span></span>

## <span data-ttu-id="382ce-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="382ce-111">PARAMETERS</span></span>

### <span data-ttu-id="382ce-112">-BackendProtocol</span><span class="sxs-lookup"><span data-stu-id="382ce-112">-BackendProtocol</span></span>
<span data-ttu-id="382ce-113">A backend biztonsági protokoll beállításai</span><span class="sxs-lookup"><span data-stu-id="382ce-113">Backend Security protocol settings.</span></span> <span data-ttu-id="382ce-114">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="382ce-114">This parameter is optional.</span></span>

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

### <span data-ttu-id="382ce-115">-CipherSuite</span><span class="sxs-lookup"><span data-stu-id="382ce-115">-CipherSuite</span></span>
<span data-ttu-id="382ce-116">A megadott sorrendben az SSL-titkosítási lakosztályok beállításai.</span><span class="sxs-lookup"><span data-stu-id="382ce-116">Ssl cipher suites settings in the specified order.</span></span> <span data-ttu-id="382ce-117">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="382ce-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="382ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="382ce-118">-DefaultProfile</span></span>
<span data-ttu-id="382ce-119">Az Azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="382ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="382ce-120">-FrontendProtocol</span><span class="sxs-lookup"><span data-stu-id="382ce-120">-FrontendProtocol</span></span>
<span data-ttu-id="382ce-121">Felület biztonsági protokolljainak beállításai</span><span class="sxs-lookup"><span data-stu-id="382ce-121">Frontend Security protocols settings.</span></span> <span data-ttu-id="382ce-122">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="382ce-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="382ce-123">-ServerProtocol</span><span class="sxs-lookup"><span data-stu-id="382ce-123">-ServerProtocol</span></span>
<span data-ttu-id="382ce-124">A kiszolgálói protokollok beállításai, például a Http2.</span><span class="sxs-lookup"><span data-stu-id="382ce-124">Server protocol settings like Http2.</span></span> <span data-ttu-id="382ce-125">Ez a paraméter nem kötelező.</span><span class="sxs-lookup"><span data-stu-id="382ce-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="382ce-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="382ce-126">CommonParameters</span></span>
<span data-ttu-id="382ce-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="382ce-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="382ce-128">További információt a [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="382ce-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="382ce-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="382ce-129">INPUTS</span></span>

### <span data-ttu-id="382ce-130">Nincs</span><span class="sxs-lookup"><span data-stu-id="382ce-130">None</span></span>

## <span data-ttu-id="382ce-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="382ce-131">OUTPUTS</span></span>

### <span data-ttu-id="382ce-132">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementSslSettings</span><span class="sxs-lookup"><span data-stu-id="382ce-132">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSettings</span></span>

## <span data-ttu-id="382ce-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="382ce-133">NOTES</span></span>

## <span data-ttu-id="382ce-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="382ce-134">RELATED LINKS</span></span>

[<span data-ttu-id="382ce-135">Új – AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="382ce-135">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

