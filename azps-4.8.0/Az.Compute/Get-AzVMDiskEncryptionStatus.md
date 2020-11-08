---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94024137"
---
# <span data-ttu-id="57290-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="57290-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="57290-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="57290-102">SYNOPSIS</span></span>
<span data-ttu-id="57290-103">A virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57290-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="57290-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="57290-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57290-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="57290-105">DESCRIPTION</span></span>
<span data-ttu-id="57290-106">A **Get-AzVMDiskEncryptionStatus** parancsmag a virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57290-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="57290-107">Megjeleníti az operációs rendszer és az adatkötetek titkosítási állapotát.</span><span class="sxs-lookup"><span data-stu-id="57290-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="57290-108">A titkosítási állapot mellett a titkosító titok URL-címe, a kulcs titkosítási kulcs URL-címe **, ahol az** operációs rendszerhez tartozó titkosítási kulcs és kulcs titkosítási kulcsa is megtalálható.</span><span class="sxs-lookup"><span data-stu-id="57290-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="57290-109">Példák</span><span class="sxs-lookup"><span data-stu-id="57290-109">EXAMPLES</span></span>

### <span data-ttu-id="57290-110">Példa 1: virtuális gép titkosítási állapotának beszerzése</span><span class="sxs-lookup"><span data-stu-id="57290-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="57290-111">Ez a parancs a VM001 nevű virtuális gép titkosítási állapotát kapja meg.</span><span class="sxs-lookup"><span data-stu-id="57290-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="57290-112">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="57290-112">PARAMETERS</span></span>

### <span data-ttu-id="57290-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57290-113">-DefaultProfile</span></span>
<span data-ttu-id="57290-114">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="57290-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="57290-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="57290-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="57290-116">A bővítmény közzétevője név.</span><span class="sxs-lookup"><span data-stu-id="57290-116">The extension publisher name.</span></span> <span data-ttu-id="57290-117">Csak akkor adja meg ezt a paramétert, ha a "Microsoft. Azure. Security" alapértelmezett értékét szeretné felülbírálni.</span><span class="sxs-lookup"><span data-stu-id="57290-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="57290-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="57290-118">-ExtensionType</span></span>
<span data-ttu-id="57290-119">A bővítmény típusa.</span><span class="sxs-lookup"><span data-stu-id="57290-119">The extension type.</span></span> <span data-ttu-id="57290-120">Adja meg ezt a paramétert, ha a Windows VMs "AzureDiskEncryption" alapértelmezett értékét szeretné felülbírálni, és a Linux VMs esetében a "AzureDiskEncryptionForLinux".</span><span class="sxs-lookup"><span data-stu-id="57290-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="57290-121">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="57290-121">-Name</span></span>
```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57290-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57290-122">-ResourceGroupName</span></span>
<span data-ttu-id="57290-123">A virtuális gép erőforráscsoport-csoportjának nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57290-123">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57290-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="57290-124">-VMName</span></span>
<span data-ttu-id="57290-125">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="57290-125">Specifies the name of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57290-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57290-126">CommonParameters</span></span>
<span data-ttu-id="57290-127">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="57290-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57290-128">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="57290-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57290-129">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="57290-129">INPUTS</span></span>

### <span data-ttu-id="57290-130">System. String</span><span class="sxs-lookup"><span data-stu-id="57290-130">System.String</span></span>

## <span data-ttu-id="57290-131">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="57290-131">OUTPUTS</span></span>

### <span data-ttu-id="57290-132">Microsoft. Azure. commands. számítási. Extension. AzureDiskEncryption. AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="57290-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="57290-133">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="57290-133">NOTES</span></span>

## <span data-ttu-id="57290-134">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="57290-134">RELATED LINKS</span></span>

[<span data-ttu-id="57290-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="57290-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="57290-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="57290-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


