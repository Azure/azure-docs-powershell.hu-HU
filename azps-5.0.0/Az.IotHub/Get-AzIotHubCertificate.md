---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187768"
---
# <span data-ttu-id="cd481-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="cd481-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="cd481-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="cd481-102">SYNOPSIS</span></span>
<span data-ttu-id="cd481-103">Az Azure IoT-központban található összes tanúsítvány vagy tanúsítvány felsorolása.</span><span class="sxs-lookup"><span data-stu-id="cd481-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="cd481-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="cd481-104">SYNTAX</span></span>

### <span data-ttu-id="cd481-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="cd481-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd481-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cd481-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd481-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cd481-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd481-108">Leírás</span><span class="sxs-lookup"><span data-stu-id="cd481-108">DESCRIPTION</span></span>
<span data-ttu-id="cd481-109">Az Azure IoT hub HITELESÍTÉSSZOLGÁLTATÓI tanúsítványainak részletes ismertetését a következő témakörben találja: https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="cd481-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="cd481-110">Példák</span><span class="sxs-lookup"><span data-stu-id="cd481-110">EXAMPLES</span></span>

### <span data-ttu-id="cd481-111">Példa 1</span><span class="sxs-lookup"><span data-stu-id="cd481-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="cd481-112">Az összes tanúsítvány listázása az MyIotHub-on</span><span class="sxs-lookup"><span data-stu-id="cd481-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="cd481-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="cd481-113">Example 2</span></span>
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

<span data-ttu-id="cd481-114">A MyCertificate részleteinek megjelenítése</span><span class="sxs-lookup"><span data-stu-id="cd481-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="cd481-115">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="cd481-115">PARAMETERS</span></span>

### <span data-ttu-id="cd481-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="cd481-116">-CertificateName</span></span>
<span data-ttu-id="cd481-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="cd481-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="cd481-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd481-118">-DefaultProfile</span></span>
<span data-ttu-id="cd481-119">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="cd481-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd481-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd481-120">-InputObject</span></span>
<span data-ttu-id="cd481-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="cd481-121">IotHub Object</span></span>

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

### <span data-ttu-id="cd481-122">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="cd481-122">-Name</span></span>
<span data-ttu-id="cd481-123">A IOT-központ neve</span><span class="sxs-lookup"><span data-stu-id="cd481-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="cd481-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd481-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd481-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="cd481-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cd481-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd481-126">-ResourceId</span></span>
<span data-ttu-id="cd481-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="cd481-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="cd481-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd481-128">CommonParameters</span></span>
<span data-ttu-id="cd481-129">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="cd481-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd481-130">További információ: about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd481-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd481-131">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd481-131">INPUTS</span></span>

### <span data-ttu-id="cd481-132">Microsoft. Azure. Command. Management. IotHub. models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="cd481-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="cd481-133">System. String</span><span class="sxs-lookup"><span data-stu-id="cd481-133">System.String</span></span>

## <span data-ttu-id="cd481-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="cd481-134">OUTPUTS</span></span>

### <span data-ttu-id="cd481-135">Microsoft. Azure. Command. Management. IotHub. models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="cd481-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="cd481-136">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="cd481-136">NOTES</span></span>

## <span data-ttu-id="cd481-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="cd481-137">RELATED LINKS</span></span>
