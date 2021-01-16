---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330053"
---
# <span data-ttu-id="c3dd8-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="c3dd8-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="c3dd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3dd8-102">SYNOPSIS</span></span>
<span data-ttu-id="c3dd8-103">Az Azure IoT-központban található összes tanúsítvány vagy adott tanúsítvány listája.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="c3dd8-104">SZINTAXIS</span><span class="sxs-lookup"><span data-stu-id="c3dd8-104">SYNTAX</span></span>

### <span data-ttu-id="c3dd8-105">ResourceSet (alapértelmezett)</span><span class="sxs-lookup"><span data-stu-id="c3dd8-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3dd8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c3dd8-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c3dd8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c3dd8-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3dd8-108">LEÍRÁS</span><span class="sxs-lookup"><span data-stu-id="c3dd8-108">DESCRIPTION</span></span>
<span data-ttu-id="c3dd8-109">Az Azure IoT-központban található hitelesítésszolgáltatói tanúsítványok részletes magyarázatát az https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c3dd8-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c3dd8-110">PÉLDÁK</span><span class="sxs-lookup"><span data-stu-id="c3dd8-110">EXAMPLES</span></span>

### <span data-ttu-id="c3dd8-111">1. példa</span><span class="sxs-lookup"><span data-stu-id="c3dd8-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="c3dd8-112">Az összes tanúsítvány felsorolása a MyIotHubban</span><span class="sxs-lookup"><span data-stu-id="c3dd8-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="c3dd8-113">2. példa</span><span class="sxs-lookup"><span data-stu-id="c3dd8-113">Example 2</span></span>
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

<span data-ttu-id="c3dd8-114">Részletek megjelenítése a MyCertificate-ről</span><span class="sxs-lookup"><span data-stu-id="c3dd8-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="c3dd8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3dd8-115">PARAMETERS</span></span>

### <span data-ttu-id="c3dd8-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c3dd8-116">-CertificateName</span></span>
<span data-ttu-id="c3dd8-117">A tanúsítvány neve</span><span class="sxs-lookup"><span data-stu-id="c3dd8-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c3dd8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3dd8-118">-DefaultProfile</span></span>
<span data-ttu-id="c3dd8-119">Az Azure-ral való kommunikációhoz használt hitelesítő adatok, fiók, bérlő és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3dd8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3dd8-120">-InputObject</span></span>
<span data-ttu-id="c3dd8-121">IotHub objektum</span><span class="sxs-lookup"><span data-stu-id="c3dd8-121">IotHub Object</span></span>

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

### <span data-ttu-id="c3dd8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="c3dd8-122">-Name</span></span>
<span data-ttu-id="c3dd8-123">Az Iot-központ neve</span><span class="sxs-lookup"><span data-stu-id="c3dd8-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c3dd8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3dd8-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3dd8-125">Az erőforráscsoport neve</span><span class="sxs-lookup"><span data-stu-id="c3dd8-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c3dd8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3dd8-126">-ResourceId</span></span>
<span data-ttu-id="c3dd8-127">IotHub erőforrás-azonosító</span><span class="sxs-lookup"><span data-stu-id="c3dd8-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c3dd8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3dd8-128">CommonParameters</span></span>
<span data-ttu-id="c3dd8-129">Ez a parancsmag a következő közös paramétereket támogatja: -Hibakeresés, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction és -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3dd8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3dd8-130">További információt a about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3dd8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3dd8-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c3dd8-131">INPUTS</span></span>

### <span data-ttu-id="c3dd8-132">Microsoft.Azure.Commands.Management.iotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c3dd8-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c3dd8-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c3dd8-133">System.String</span></span>

## <span data-ttu-id="c3dd8-134">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="c3dd8-134">OUTPUTS</span></span>

### <span data-ttu-id="c3dd8-135">Microsoft.Azure.Commands.Management.iotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c3dd8-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="c3dd8-136">MEGJEGYZÉSEK</span><span class="sxs-lookup"><span data-stu-id="c3dd8-136">NOTES</span></span>

## <span data-ttu-id="c3dd8-137">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="c3dd8-137">RELATED LINKS</span></span>
