---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 55b95cec3e699872688fad5daeb0d2f7e89059c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498056"
---
# <span data-ttu-id="a914b-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a914b-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="a914b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="a914b-102">SYNOPSIS</span></span>
<span data-ttu-id="a914b-103">Létrehoz egy API-kezelési tanúsítványt, amelyet a rendszer a backend-hitelesítés során használni fog.</span><span class="sxs-lookup"><span data-stu-id="a914b-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a914b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="a914b-104">SYNTAX</span></span>

### <span data-ttu-id="a914b-105">Beolvasás fájlból (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="a914b-105">Load from file (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a914b-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="a914b-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a914b-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="a914b-107">DESCRIPTION</span></span>
<span data-ttu-id="a914b-108">A **New-AzureRmApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a914b-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="a914b-109">Példák</span><span class="sxs-lookup"><span data-stu-id="a914b-109">EXAMPLES</span></span>

### <span data-ttu-id="a914b-110">1. példa: tanúsítvány létrehozása és feltöltése</span><span class="sxs-lookup"><span data-stu-id="a914b-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="a914b-111">A parancs API-kezelési tanúsítványt hoz létre, és feltölti azt.</span><span class="sxs-lookup"><span data-stu-id="a914b-111">This command creates an API Management certificate and uploads it.</span></span>

## <span data-ttu-id="a914b-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="a914b-112">PARAMETERS</span></span>

### <span data-ttu-id="a914b-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="a914b-113">-CertificateId</span></span>
<span data-ttu-id="a914b-114">A létrehozandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a914b-114">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="a914b-115">Ha nem adja meg ezt a paramétert, a rendszer azonosítót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="a914b-115">If you do not specify this parameter, an ID is generated for you.</span></span>

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

### <span data-ttu-id="a914b-116">-Környezet</span><span class="sxs-lookup"><span data-stu-id="a914b-116">-Context</span></span>
<span data-ttu-id="a914b-117">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="a914b-117">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a914b-118">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="a914b-118">-PfxBytes</span></span>
<span data-ttu-id="a914b-119">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="a914b-119">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="a914b-120">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a914b-120">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="a914b-121">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="a914b-121">-PfxFilePath</span></span>
<span data-ttu-id="a914b-122">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="a914b-122">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="a914b-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="a914b-123">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: Load from file
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a914b-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="a914b-124">-PfxPassword</span></span>
<span data-ttu-id="a914b-125">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="a914b-125">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="a914b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a914b-126">-DefaultProfile</span></span>
<span data-ttu-id="a914b-127">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="a914b-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a914b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a914b-128">CommonParameters</span></span>
<span data-ttu-id="a914b-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="a914b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a914b-130">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a914b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a914b-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="a914b-131">INPUTS</span></span>

## <span data-ttu-id="a914b-132">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="a914b-132">OUTPUTS</span></span>

### <span data-ttu-id="a914b-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a914b-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="a914b-134">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="a914b-134">NOTES</span></span>

## <span data-ttu-id="a914b-135">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="a914b-135">RELATED LINKS</span></span>

[<span data-ttu-id="a914b-136">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a914b-136">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="a914b-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a914b-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="a914b-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="a914b-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


