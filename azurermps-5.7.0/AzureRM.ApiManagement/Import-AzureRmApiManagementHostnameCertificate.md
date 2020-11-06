---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
ms.assetid: 98367100-4FFD-46F6-8974-603B32533626
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/import-azurermapimanagementhostnamecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Import-AzureRmApiManagementHostnameCertificate.md
ms.openlocfilehash: 9c5f819a34ea0e394888e8156dad7a897d18167f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503904"
---
# <span data-ttu-id="40582-101">Import-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="40582-101">Import-AzureRmApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="40582-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="40582-102">SYNOPSIS</span></span>
<span data-ttu-id="40582-103">Egy, az API-kezelési szolgáltatáshoz tartozó PFX-formátumú tanúsítványt importál.</span><span class="sxs-lookup"><span data-stu-id="40582-103">Imports a certificate in a PFX format for an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40582-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="40582-104">SYNTAX</span></span>

```
Import-AzureRmApiManagementHostnameCertificate -ResourceGroupName <String> -Name <String>
 -HostnameType <PsApiManagementHostnameType> -PfxPath <String> -PfxPassword <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40582-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="40582-105">DESCRIPTION</span></span>
<span data-ttu-id="40582-106">Az **import-AzureRmApiManagementHostnameCertificate** parancsmag egy, az API-kezelési szolgáltatás pfx-formátumú tanúsítványát importálja.</span><span class="sxs-lookup"><span data-stu-id="40582-106">The **Import-AzureRmApiManagementHostnameCertificate** cmdlet imports a certificate in a PFX format for an API Management Service.</span></span>
<span data-ttu-id="40582-107">A tanúsítványt az egyéni állomásnevek-konfigurációhoz kell használni.</span><span class="sxs-lookup"><span data-stu-id="40582-107">The certificate is to be used for custom hostnames configuration.</span></span>

## <span data-ttu-id="40582-108">Példák</span><span class="sxs-lookup"><span data-stu-id="40582-108">EXAMPLES</span></span>

### <span data-ttu-id="40582-109">1. példa: API-kezelési gépnév tanúsítvány importálása</span><span class="sxs-lookup"><span data-stu-id="40582-109">Example 1: Import a API Management hostname certificate</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName Contoso -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
```

<span data-ttu-id="40582-110">Ezzel a paranccsal importálhat egy tanúsítványt az egyéni állomásnévhez.</span><span class="sxs-lookup"><span data-stu-id="40582-110">This command imports a certificate for a proxy custom hostname.</span></span>

## <span data-ttu-id="40582-111">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="40582-111">PARAMETERS</span></span>

### <span data-ttu-id="40582-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40582-112">-DefaultProfile</span></span>
<span data-ttu-id="40582-113">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="40582-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="40582-114">-HostnameType</span><span class="sxs-lookup"><span data-stu-id="40582-114">-HostnameType</span></span>
<span data-ttu-id="40582-115">Azt az állomásnév-típust adja meg, amelyre a parancsmag betölti a tanúsítványt.</span><span class="sxs-lookup"><span data-stu-id="40582-115">Specifies the host name type that this cmdlet loads the certificate for.</span></span>

<span data-ttu-id="40582-116">Az érvényes értékek a következők:</span><span class="sxs-lookup"><span data-stu-id="40582-116">Valid values are:</span></span> 

- <span data-ttu-id="40582-117">Proxy</span><span class="sxs-lookup"><span data-stu-id="40582-117">Proxy</span></span>
- <span data-ttu-id="40582-118">Portál</span><span class="sxs-lookup"><span data-stu-id="40582-118">Portal</span></span>

```yaml
Type: PsApiManagementHostnameType
Parameter Sets: (All)
Aliases: 
Accepted values: Proxy, Portal

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40582-119">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="40582-119">-Name</span></span>
<span data-ttu-id="40582-120">Itt adhatja meg az API-kezelés telepített példányának a nevét, amelyet a parancsmag importál.</span><span class="sxs-lookup"><span data-stu-id="40582-120">Specifies the name of the API Management deployment that this cmdlet imports.</span></span>

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

### <span data-ttu-id="40582-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40582-121">-PassThru</span></span>
<span data-ttu-id="40582-122">Egy olyan objektumot ad eredményül, amely a munkaterületet jelképezi.</span><span class="sxs-lookup"><span data-stu-id="40582-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="40582-123">Ez a parancsmag alapértelmezés szerint nem hoz létre semmilyen kimenetet.</span><span class="sxs-lookup"><span data-stu-id="40582-123">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40582-124">-PfxPassword</span><span class="sxs-lookup"><span data-stu-id="40582-124">-PfxPassword</span></span>
<span data-ttu-id="40582-125">A. pfx tanúsítványfájl jelszavát adja meg.</span><span class="sxs-lookup"><span data-stu-id="40582-125">Specifies the password for the .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40582-126">-PfxPath</span><span class="sxs-lookup"><span data-stu-id="40582-126">-PfxPath</span></span>
<span data-ttu-id="40582-127">A. pfx tanúsítványfájl elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="40582-127">Specifies the path to a .pfx certificate file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40582-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40582-128">-ResourceGroupName</span></span>
<span data-ttu-id="40582-129">Annak az erőforrás-csoportnak a nevét adja meg, amely alatt az API-kezelési példány létezik.</span><span class="sxs-lookup"><span data-stu-id="40582-129">Specifies the name of the of resource group under which the API Management deployment exists.</span></span>

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

### <span data-ttu-id="40582-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40582-130">CommonParameters</span></span>
<span data-ttu-id="40582-131">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="40582-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40582-132">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40582-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40582-133">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="40582-133">INPUTS</span></span>

### <span data-ttu-id="40582-134">Nincs</span><span class="sxs-lookup"><span data-stu-id="40582-134">None</span></span>
<span data-ttu-id="40582-135">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="40582-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40582-136">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="40582-136">OUTPUTS</span></span>

### <span data-ttu-id="40582-137">Microsoft. Azure. Command. ApiManagement. models. PsApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="40582-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameCertificate</span></span>

## <span data-ttu-id="40582-138">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="40582-138">NOTES</span></span>

## <span data-ttu-id="40582-139">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="40582-139">RELATED LINKS</span></span>

[<span data-ttu-id="40582-140">Új – AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="40582-140">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)

[<span data-ttu-id="40582-141">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="40582-141">Set-AzureRmApiManagementHostnames</span></span>](./Set-AzureRmApiManagementHostnames.md)


