---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementCertificate.md
ms.openlocfilehash: 1fe178b80a39d4587a97207b6bd2d8cf6f4c9731
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93671674"
---
# <span data-ttu-id="d3723-101">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d3723-101">New-AzApiManagementCertificate</span></span>

## <span data-ttu-id="d3723-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="d3723-102">SYNOPSIS</span></span>
<span data-ttu-id="d3723-103">Létrehoz egy API-kezelési tanúsítványt, amelyet a rendszer a backend-hitelesítés során használni fog.</span><span class="sxs-lookup"><span data-stu-id="d3723-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

## <span data-ttu-id="d3723-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="d3723-104">SYNTAX</span></span>

### <span data-ttu-id="d3723-105">LoadFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="d3723-105">LoadFromFile (Default)</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3723-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="d3723-106">Raw</span></span>
```
New-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>] -PfxBytes <Byte[]>
 -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3723-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="d3723-107">DESCRIPTION</span></span>
<span data-ttu-id="d3723-108">A **New-AzApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d3723-108">The **New-AzApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="d3723-109">Példák</span><span class="sxs-lookup"><span data-stu-id="d3723-109">EXAMPLES</span></span>

### <span data-ttu-id="d3723-110">1. példa: tanúsítvány létrehozása és feltöltése</span><span class="sxs-lookup"><span data-stu-id="d3723-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="d3723-111">A parancs feltölti a tanúsítványt az API-menedzsmentbe.</span><span class="sxs-lookup"><span data-stu-id="d3723-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="d3723-112">Ez a tanúsítvány a backend-ben való kölcsönös hitelesítéshez használható a házirendek használatával.</span><span class="sxs-lookup"><span data-stu-id="d3723-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="d3723-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="d3723-113">PARAMETERS</span></span>

### <span data-ttu-id="d3723-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="d3723-114">-CertificateId</span></span>
<span data-ttu-id="d3723-115">A létrehozandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3723-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="d3723-116">Ha nem adja meg ezt a paramétert, a rendszer azonosítót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="d3723-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3723-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="d3723-117">-Context</span></span>
<span data-ttu-id="d3723-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="d3723-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d3723-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3723-119">-DefaultProfile</span></span>
<span data-ttu-id="d3723-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="d3723-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3723-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="d3723-121">-PfxBytes</span></span>
<span data-ttu-id="d3723-122">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="d3723-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="d3723-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d3723-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: Raw
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3723-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="d3723-124">-PfxFilePath</span></span>
<span data-ttu-id="d3723-125">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3723-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="d3723-126">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="d3723-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: LoadFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3723-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="d3723-127">-PfxPassword</span></span>
<span data-ttu-id="d3723-128">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="d3723-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="d3723-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3723-129">CommonParameters</span></span>
<span data-ttu-id="d3723-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="d3723-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3723-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3723-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3723-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3723-132">INPUTS</span></span>

### <span data-ttu-id="d3723-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d3723-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d3723-134">System. String</span><span class="sxs-lookup"><span data-stu-id="d3723-134">System.String</span></span>

### <span data-ttu-id="d3723-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="d3723-135">System.Byte[]</span></span>

## <span data-ttu-id="d3723-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="d3723-136">OUTPUTS</span></span>

### <span data-ttu-id="d3723-137">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d3723-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="d3723-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="d3723-138">NOTES</span></span>

## <span data-ttu-id="d3723-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="d3723-139">RELATED LINKS</span></span>

[<span data-ttu-id="d3723-140">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d3723-140">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="d3723-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d3723-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="d3723-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="d3723-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


