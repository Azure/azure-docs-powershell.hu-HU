---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementCertificate.md
ms.openlocfilehash: f7712a7938617d979dad2feabf4d2b2126e20433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93492059"
---
# <span data-ttu-id="465cc-101">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="465cc-101">Set-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="465cc-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="465cc-102">SYNOPSIS</span></span>
<span data-ttu-id="465cc-103">Módosítja az API-kezelési tanúsítványokat, amelyek a backend-tel való kölcsönös hitelesítésre vannak konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="465cc-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="465cc-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="465cc-104">SYNTAX</span></span>

### <span data-ttu-id="465cc-105">LoadFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="465cc-105">LoadFromFile (Default)</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxFilePath <String> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="465cc-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="465cc-106">Raw</span></span>
```
Set-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 -PfxBytes <Byte[]> -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="465cc-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="465cc-107">DESCRIPTION</span></span>
<span data-ttu-id="465cc-108">A **set-AzureRmApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt módosít.</span><span class="sxs-lookup"><span data-stu-id="465cc-108">The **Set-AzureRmApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="465cc-109">Példák</span><span class="sxs-lookup"><span data-stu-id="465cc-109">EXAMPLES</span></span>

### <span data-ttu-id="465cc-110">Példa 1: tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="465cc-110">Example 1: Modify a certificate</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="465cc-111">Ez a parancs módosítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="465cc-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="465cc-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="465cc-112">PARAMETERS</span></span>

### <span data-ttu-id="465cc-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="465cc-113">-CertificateId</span></span>
<span data-ttu-id="465cc-114">A módosítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="465cc-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="465cc-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="465cc-115">-Context</span></span>
<span data-ttu-id="465cc-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="465cc-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="465cc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="465cc-117">-DefaultProfile</span></span>
<span data-ttu-id="465cc-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="465cc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="465cc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="465cc-119">-PassThru</span></span>
<span data-ttu-id="465cc-120">passthru</span><span class="sxs-lookup"><span data-stu-id="465cc-120">passthru</span></span>

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

### <span data-ttu-id="465cc-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="465cc-121">-PfxBytes</span></span>
<span data-ttu-id="465cc-122">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="465cc-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="465cc-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="465cc-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="465cc-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="465cc-124">-PfxFilePath</span></span>
<span data-ttu-id="465cc-125">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="465cc-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="465cc-126">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="465cc-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="465cc-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="465cc-127">-PfxPassword</span></span>
<span data-ttu-id="465cc-128">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="465cc-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="465cc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="465cc-129">CommonParameters</span></span>
<span data-ttu-id="465cc-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="465cc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="465cc-131">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="465cc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="465cc-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="465cc-132">INPUTS</span></span>

### <span data-ttu-id="465cc-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="465cc-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="465cc-134">System. String</span><span class="sxs-lookup"><span data-stu-id="465cc-134">System.String</span></span>

### <span data-ttu-id="465cc-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="465cc-135">System.Byte[]</span></span>

### <span data-ttu-id="465cc-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="465cc-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="465cc-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="465cc-137">OUTPUTS</span></span>

### <span data-ttu-id="465cc-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="465cc-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="465cc-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="465cc-139">NOTES</span></span>

## <span data-ttu-id="465cc-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="465cc-140">RELATED LINKS</span></span>

[<span data-ttu-id="465cc-141">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="465cc-141">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="465cc-142">Új – AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="465cc-142">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="465cc-143">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="465cc-143">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)


