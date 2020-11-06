---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 5CBEDFF8-C441-44CC-B011-5F5AAFA2E5C6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7ddfb327931fc7ebb9eac76cdd6818521332483
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495487"
---
# <span data-ttu-id="1f10c-101">New-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f10c-101">New-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="1f10c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="1f10c-102">SYNOPSIS</span></span>
<span data-ttu-id="1f10c-103">Létrehoz egy API-kezelési tanúsítványt, amelyet a rendszer a backend-hitelesítés során használni fog.</span><span class="sxs-lookup"><span data-stu-id="1f10c-103">Creates an API Management certificate to be used during Authentication with Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f10c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="1f10c-104">SYNTAX</span></span>

### <span data-ttu-id="1f10c-105">LoadFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="1f10c-105">LoadFromFile (Default)</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxFilePath <String> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f10c-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="1f10c-106">Raw</span></span>
```
New-AzureRmApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 -PfxBytes <Byte[]> -PfxPassword <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f10c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="1f10c-107">DESCRIPTION</span></span>
<span data-ttu-id="1f10c-108">A **New-AzureRmApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f10c-108">The **New-AzureRmApiManagementCertificate** cmdlet creates an Azure API Management certificate.</span></span>

## <span data-ttu-id="1f10c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="1f10c-109">EXAMPLES</span></span>

### <span data-ttu-id="1f10c-110">1. példa: tanúsítvány létrehozása és feltöltése</span><span class="sxs-lookup"><span data-stu-id="1f10c-110">Example 1: Create and upload a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementCertificate -Context $ApiMgmtContext -PfxFilePath "C:\contoso\certificates\apimanagement.pfx" -PfxPassword "1111"
```

<span data-ttu-id="1f10c-111">A parancs feltölti a tanúsítványt az API-menedzsmentbe.</span><span class="sxs-lookup"><span data-stu-id="1f10c-111">This command uploads a certificate to Api Management.</span></span> <span data-ttu-id="1f10c-112">Ez a tanúsítvány a backend-ben való kölcsönös hitelesítéshez használható a házirendek használatával.</span><span class="sxs-lookup"><span data-stu-id="1f10c-112">This certificate can be used for mutual authentication with backend using policies.</span></span>

## <span data-ttu-id="1f10c-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="1f10c-113">PARAMETERS</span></span>

### <span data-ttu-id="1f10c-114">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1f10c-114">-CertificateId</span></span>
<span data-ttu-id="1f10c-115">A létrehozandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f10c-115">Specifies the ID of the certificate to create.</span></span>
<span data-ttu-id="1f10c-116">Ha nem adja meg ezt a paramétert, a rendszer azonosítót hoz létre.</span><span class="sxs-lookup"><span data-stu-id="1f10c-116">If you do not specify this parameter, an ID is generated for you.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-117">-Környezet</span><span class="sxs-lookup"><span data-stu-id="1f10c-117">-Context</span></span>
<span data-ttu-id="1f10c-118">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="1f10c-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f10c-119">-DefaultProfile</span></span>
<span data-ttu-id="1f10c-120">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="1f10c-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="1f10c-121">-PfxBytes</span></span>
<span data-ttu-id="1f10c-122">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="1f10c-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="1f10c-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="1f10c-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

```yaml
Type: Byte[]
Parameter Sets: Raw
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="1f10c-124">-PfxFilePath</span></span>
<span data-ttu-id="1f10c-125">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f10c-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="1f10c-126">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="1f10c-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

```yaml
Type: String
Parameter Sets: LoadFromFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="1f10c-127">-PfxPassword</span></span>
<span data-ttu-id="1f10c-128">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="1f10c-128">Specifies the password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f10c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f10c-129">CommonParameters</span></span>
<span data-ttu-id="1f10c-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="1f10c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f10c-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f10c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f10c-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f10c-132">INPUTS</span></span>

### <span data-ttu-id="1f10c-133">Nincs</span><span class="sxs-lookup"><span data-stu-id="1f10c-133">None</span></span>
<span data-ttu-id="1f10c-134">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="1f10c-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1f10c-135">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="1f10c-135">OUTPUTS</span></span>

### <span data-ttu-id="1f10c-136">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f10c-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="1f10c-137">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="1f10c-137">NOTES</span></span>

## <span data-ttu-id="1f10c-138">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="1f10c-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f10c-139">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f10c-139">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1f10c-140">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f10c-140">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="1f10c-141">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1f10c-141">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


