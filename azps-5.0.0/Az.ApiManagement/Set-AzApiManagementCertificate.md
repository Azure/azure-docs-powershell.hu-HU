---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 12FC21EB-0B4E-4275-88FB-7FF42730A6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementCertificate.md
ms.openlocfilehash: 3c31da297b47c5d35c7d7b4eea5c55ca87d9521d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94186277"
---
# <span data-ttu-id="4ba30-101">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ba30-101">Set-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4ba30-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="4ba30-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba30-103">Módosítja az API-kezelési tanúsítványokat, amelyek a backend-tel való kölcsönös hitelesítésre vannak konfigurálva.</span><span class="sxs-lookup"><span data-stu-id="4ba30-103">Modifies an API Management certificate which is configured for mutual authentication with backend.</span></span>

## <span data-ttu-id="4ba30-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="4ba30-104">SYNTAX</span></span>

### <span data-ttu-id="4ba30-105">LoadFromFile (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="4ba30-105">LoadFromFile (Default)</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxFilePath <String>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ba30-106">Nyers</span><span class="sxs-lookup"><span data-stu-id="4ba30-106">Raw</span></span>
```
Set-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> -PfxBytes <Byte[]>
 -PfxPassword <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ba30-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="4ba30-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba30-108">A **set-AzApiManagementCertificate** parancsmag egy Azure API-kezelési tanúsítványt módosít.</span><span class="sxs-lookup"><span data-stu-id="4ba30-108">The **Set-AzApiManagementCertificate** cmdlet modifies an Azure API Management certificate.</span></span>

## <span data-ttu-id="4ba30-109">Példák</span><span class="sxs-lookup"><span data-stu-id="4ba30-109">EXAMPLES</span></span>

### <span data-ttu-id="4ba30-110">Példa 1: tanúsítvány módosítása</span><span class="sxs-lookup"><span data-stu-id="4ba30-110">Example 1: Modify a certificate</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -PfxFilePath "C:\contoso\certificates\apimanagementnew.pfx" -PfxPassword "2222"
```

<span data-ttu-id="4ba30-111">Ez a parancs módosítja a megadott API-kezelési tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="4ba30-111">This command modifies the specified API Management certificate.</span></span>

## <span data-ttu-id="4ba30-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="4ba30-112">PARAMETERS</span></span>

### <span data-ttu-id="4ba30-113">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4ba30-113">-CertificateId</span></span>
<span data-ttu-id="4ba30-114">A módosítandó tanúsítvány AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ba30-114">Specifies the ID of the certificate to modify.</span></span>

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

### <span data-ttu-id="4ba30-115">-Környezet</span><span class="sxs-lookup"><span data-stu-id="4ba30-115">-Context</span></span>
<span data-ttu-id="4ba30-116">Egy **PsApiManagementContext** -objektumot ad meg.</span><span class="sxs-lookup"><span data-stu-id="4ba30-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ba30-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba30-117">-DefaultProfile</span></span>
<span data-ttu-id="4ba30-118">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="4ba30-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ba30-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4ba30-119">-PassThru</span></span>
<span data-ttu-id="4ba30-120">passthru</span><span class="sxs-lookup"><span data-stu-id="4ba30-120">passthru</span></span>

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

### <span data-ttu-id="4ba30-121">-PfxBytes</span><span class="sxs-lookup"><span data-stu-id="4ba30-121">-PfxBytes</span></span>
<span data-ttu-id="4ba30-122">A tanúsítványfájl. pfx formátumban adja meg a tanúsítványfájl bájtjainak tömbjét.</span><span class="sxs-lookup"><span data-stu-id="4ba30-122">Specifies an array of bytes of the certificate file in .pfx format.</span></span>
<span data-ttu-id="4ba30-123">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxFilePath* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ba30-123">This parameter is required if you do not specify the *PfxFilePath* parameter.</span></span>

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

### <span data-ttu-id="4ba30-124">-PfxFilePath</span><span class="sxs-lookup"><span data-stu-id="4ba30-124">-PfxFilePath</span></span>
<span data-ttu-id="4ba30-125">A létrehozáshoz és a feltöltéshez a. pfx formátumú tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ba30-125">Specifies the path to the certificate file in .pfx format to create and upload.</span></span>
<span data-ttu-id="4ba30-126">Ez a paraméter akkor szükséges, ha nem adja meg a *PfxBytes* paramétert.</span><span class="sxs-lookup"><span data-stu-id="4ba30-126">This parameter is required if you do not specify the *PfxBytes* parameter.</span></span>

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

### <span data-ttu-id="4ba30-127">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="4ba30-127">-PfxPassword</span></span>
<span data-ttu-id="4ba30-128">A tanúsítvány jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="4ba30-128">Specifies the password for the certificate.</span></span>

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

### <span data-ttu-id="4ba30-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba30-129">CommonParameters</span></span>
<span data-ttu-id="4ba30-130">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="4ba30-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba30-131">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="4ba30-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba30-132">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ba30-132">INPUTS</span></span>

### <span data-ttu-id="4ba30-133">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4ba30-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4ba30-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4ba30-134">System.String</span></span>

### <span data-ttu-id="4ba30-135">System. byte []</span><span class="sxs-lookup"><span data-stu-id="4ba30-135">System.Byte[]</span></span>

### <span data-ttu-id="4ba30-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4ba30-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4ba30-137">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="4ba30-137">OUTPUTS</span></span>

### <span data-ttu-id="4ba30-138">Microsoft. Azure. Command. ApiManagement. ServiceManagement. models. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ba30-138">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4ba30-139">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="4ba30-139">NOTES</span></span>

## <span data-ttu-id="4ba30-140">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="4ba30-140">RELATED LINKS</span></span>

[<span data-ttu-id="4ba30-141">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ba30-141">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="4ba30-142">Új – AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ba30-142">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4ba30-143">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4ba30-143">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)


