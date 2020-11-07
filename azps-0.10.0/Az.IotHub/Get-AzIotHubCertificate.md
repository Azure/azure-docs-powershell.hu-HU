---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 517f4822817a97c6ac22facb206b513a06f85d6d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842253"
---
# <span data-ttu-id="2ac9d-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="2ac9d-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="2ac9d-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2ac9d-102">SYNOPSIS</span></span>
<span data-ttu-id="2ac9d-103">Az Azure IoT-központban található összes tanúsítvány vagy tanúsítvány felsorolása.</span><span class="sxs-lookup"><span data-stu-id="2ac9d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="2ac9d-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2ac9d-104">SYNTAX</span></span>

### <span data-ttu-id="2ac9d-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="2ac9d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac9d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2ac9d-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2ac9d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2ac9d-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2ac9d-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="2ac9d-108">DESCRIPTION</span></span>
<span data-ttu-id="2ac9d-109">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="2ac9d-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="2ac9d-110">Példák</span><span class="sxs-lookup"><span data-stu-id="2ac9d-110">EXAMPLES</span></span>

### <span data-ttu-id="2ac9d-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="2ac9d-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="2ac9d-112">Az összes tanúsítvány listázása az MyIotHub-on</span><span class="sxs-lookup"><span data-stu-id="2ac9d-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="2ac9d-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="2ac9d-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="2ac9d-114">A MyCertificate részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="2ac9d-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="2ac9d-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2ac9d-115">PARAMETERS</span></span>

### <span data-ttu-id="2ac9d-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="2ac9d-116">-CertificateName</span></span>
<span data-ttu-id="2ac9d-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="2ac9d-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac9d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ac9d-118">-DefaultProfile</span></span>
<span data-ttu-id="2ac9d-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2ac9d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ac9d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2ac9d-120">-InputObject</span></span>
<span data-ttu-id="2ac9d-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="2ac9d-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac9d-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2ac9d-122">-Name</span></span>
<span data-ttu-id="2ac9d-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="2ac9d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ac9d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ac9d-124">-ResourceGroupName</span></span>
<span data-ttu-id="2ac9d-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="2ac9d-125">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac9d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2ac9d-126">-ResourceId</span></span>
<span data-ttu-id="2ac9d-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="2ac9d-127">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ac9d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ac9d-128">CommonParameters</span></span>
<span data-ttu-id="2ac9d-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2ac9d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ac9d-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ac9d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ac9d-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ac9d-131">INPUTS</span></span>

### <span data-ttu-id="2ac9d-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="2ac9d-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="2ac9d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2ac9d-133">System.String</span></span>

## <span data-ttu-id="2ac9d-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2ac9d-134">OUTPUTS</span></span>

### <span data-ttu-id="2ac9d-135">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="2ac9d-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="2ac9d-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2ac9d-136">NOTES</span></span>

## <span data-ttu-id="2ac9d-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2ac9d-137">RELATED LINKS</span></span>
