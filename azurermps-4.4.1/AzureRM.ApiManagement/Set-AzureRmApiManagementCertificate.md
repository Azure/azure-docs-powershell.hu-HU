---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: ca9305b2d5863276c5d898e310dfab8be7488382
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93679988"
---
# <span data-ttu-id="bab26-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bab26-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="bab26-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="bab26-102">SYNOPSIS</span></span>
<span data-ttu-id="bab26-103">API-kezelési tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="bab26-103">Modifies an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bab26-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="bab26-104">SYNTAX</span></span>

### <span data-ttu-id="bab26-105">Beolvasás fájlból (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="bab26-105">Load from file (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bab26-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="bab26-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bab26-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="bab26-107">DESCRIPTION</span></span>
<span data-ttu-id="bab26-108">A **set-AzureRmApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt módosít.</span><span class="sxs-lookup"><span data-stu-id="bab26-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="bab26-109">Példák</span><span class="sxs-lookup"><span data-stu-id="bab26-109">EXAMPLES</span></span>

### <span data-ttu-id="bab26-110">Példa 1: tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="bab26-110">Example 1: Modify a certificate</span></span>
```
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="bab26-111">Ez a parancs módosítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="bab26-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="bab26-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="bab26-112">PARAMETERS</span></span>

### <span data-ttu-id="bab26-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="bab26-113">-CertificateId</span></span>
<span data-ttu-id="bab26-114">A módosítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bab26-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="bab26-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="bab26-115">-Context</span></span>
<span data-ttu-id="bab26-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="bab26-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="bab26-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bab26-117">-PassThru</span></span>
<span data-ttu-id="bab26-118">passthru</span><span class="sxs-lookup"><span data-stu-id="bab26-118">passthru</span></span>

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

### <span data-ttu-id="bab26-119">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="bab26-119">-PfxBytes</span></span>
<span data-ttu-id="bab26-120">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="bab26-120">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="bab26-121">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bab26-121">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="bab26-122">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="bab26-122">-PfxFilePath</span></span>
<span data-ttu-id="bab26-123">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="bab26-123">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="bab26-124">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="bab26-124">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="bab26-125">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="bab26-125">-PfxPassword</span></span>
<span data-ttu-id="bab26-126">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="bab26-126">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="bab26-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bab26-127">-DefaultProfile</span></span>
<span data-ttu-id="bab26-128">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="bab26-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bab26-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bab26-129">CommonParameters</span></span>
<span data-ttu-id="bab26-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="bab26-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bab26-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bab26-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bab26-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="bab26-132">INPUTS</span></span>

## <span data-ttu-id="bab26-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="bab26-133">OUTPUTS</span></span>

### <span data-ttu-id="bab26-134">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bab26-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="bab26-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="bab26-135">NOTES</span></span>

## <span data-ttu-id="bab26-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="bab26-136">RELATED LINKS</span></span>

[<span data-ttu-id="bab26-137">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bab26-137">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="bab26-138">Új – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bab26-138">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="bab26-139">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="bab26-139">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


