---
external help file: Microsoft.Azure.Commands.ServerManagement.dll-Help.xml
Module Name: AzureRM
ms.assetid: ECF85C07-2C9E-487D-A2ED-77875C380244
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servermanagement/save-azurermservermanagementgatewayprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServerManagement/Commands.ServerManagement/help/Save-AzureRmServerManagementGatewayProfile.md
ms.openlocfilehash: 8dd9aeaaf987fba155ca80b0c8739d44c80945e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93494346"
---
# <span data-ttu-id="9549c-101">Save-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="9549c-101">Save-AzureRmServerManagementGatewayProfile</span></span>

## <span data-ttu-id="9549c-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="9549c-102">SYNOPSIS</span></span>
<span data-ttu-id="9549c-103">Letölti a Kiszolgálókezelő-átjáró profilját, és egy helyi fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="9549c-103">Downloads the profile for a Server Management gateway and saves it to a local file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9549c-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="9549c-104">SYNTAX</span></span>

### <span data-ttu-id="9549c-105">ByName</span><span class="sxs-lookup"><span data-stu-id="9549c-105">ByName</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-ResourceGroupName] <String>
 [-GatewayName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9549c-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="9549c-106">ByObject</span></span>
```
Save-AzureRmServerManagementGatewayProfile [-OutputFile] <FileInfo> [-Gateway] <Gateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9549c-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="9549c-107">DESCRIPTION</span></span>
<span data-ttu-id="9549c-108">A **Save-AzureRmServerManagementGatewayProfile** parancsmag letölti az Azure Server Management Gateway profilját, és egy helyi fájlba menti.</span><span class="sxs-lookup"><span data-stu-id="9549c-108">The **Save-AzureRmServerManagementGatewayProfile** cmdlet downloads the profile for an Azure Server Management gateway and stores it to a local file.</span></span>

## <span data-ttu-id="9549c-109">Példák</span><span class="sxs-lookup"><span data-stu-id="9549c-109">EXAMPLES</span></span>

## <span data-ttu-id="9549c-110">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="9549c-110">PARAMETERS</span></span>

### <span data-ttu-id="9549c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9549c-111">-DefaultProfile</span></span>
<span data-ttu-id="9549c-112">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="9549c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9549c-113">-Gateway</span><span class="sxs-lookup"><span data-stu-id="9549c-113">-Gateway</span></span>
<span data-ttu-id="9549c-114">Azt az átjárót adja meg, amelyre a parancsmag a megfelelő profilt kapja.</span><span class="sxs-lookup"><span data-stu-id="9549c-114">Specifies the gateway that this cmdlet gets the profile for.</span></span>

<span data-ttu-id="9549c-115">Használható a ResourceGroupName és a GatewayName megadása helyett</span><span class="sxs-lookup"><span data-stu-id="9549c-115">May be used instead of specifying ResourceGroupName and GatewayName</span></span>

```yaml
Type: Gateway
Parameter Sets: ByObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9549c-116">-GatewayName</span><span class="sxs-lookup"><span data-stu-id="9549c-116">-GatewayName</span></span>
<span data-ttu-id="9549c-117">Itt adhatja meg annak az átjárónak a nevét, amelyhez ez a parancsmag a profilját kapja.</span><span class="sxs-lookup"><span data-stu-id="9549c-117">Specifies the name of the gateway that this cmdlet gets the profile for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9549c-118">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9549c-118">-OutputFile</span></span>
<span data-ttu-id="9549c-119">Azt a helyi fájlt adja meg, amelybe menteni szeretné a profil-adatforrást.</span><span class="sxs-lookup"><span data-stu-id="9549c-119">Specifies the local file in which to save the profile data.</span></span>

```yaml
Type: FileInfo
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9549c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9549c-120">-ResourceGroupName</span></span>
<span data-ttu-id="9549c-121">Annak az erőforráscsoport-csoportnak a neve, amelyhez az átjáró tartozik.</span><span class="sxs-lookup"><span data-stu-id="9549c-121">Specifies the name of the resource group that the gateway belongs to.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9549c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9549c-122">CommonParameters</span></span>
<span data-ttu-id="9549c-123">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="9549c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9549c-124">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9549c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9549c-125">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="9549c-125">INPUTS</span></span>

### <span data-ttu-id="9549c-126">Átjáró</span><span class="sxs-lookup"><span data-stu-id="9549c-126">Gateway</span></span>
<span data-ttu-id="9549c-127">Az "átjáró" paraméter elfogadja az "átjáró" típusú értéket a csővezetéken</span><span class="sxs-lookup"><span data-stu-id="9549c-127">Parameter 'Gateway' accepts value of type 'Gateway' from the pipeline</span></span>

## <span data-ttu-id="9549c-128">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="9549c-128">OUTPUTS</span></span>

### <span data-ttu-id="9549c-129">System. IO. FileInfo</span><span class="sxs-lookup"><span data-stu-id="9549c-129">System.IO.FileInfo</span></span>

## <span data-ttu-id="9549c-130">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="9549c-130">NOTES</span></span>

## <span data-ttu-id="9549c-131">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="9549c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9549c-132">Telepítés – AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="9549c-132">Install-AzureRmServerManagementGatewayProfile</span></span>](./Install-AzureRmServerManagementGatewayProfile.md)

[<span data-ttu-id="9549c-133">Reset-AzureRmServerManagementGatewayProfile</span><span class="sxs-lookup"><span data-stu-id="9549c-133">Reset-AzureRmServerManagementGatewayProfile</span></span>](./Reset-AzureRmServerManagementGatewayProfile.md)


