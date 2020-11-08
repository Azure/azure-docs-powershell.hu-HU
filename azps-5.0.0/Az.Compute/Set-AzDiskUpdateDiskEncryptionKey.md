---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatediskencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateDiskEncryptionKey.md
ms.openlocfilehash: 51a501e2b01ef044685f4172d42bad5342cb462c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94187508"
---
# <span data-ttu-id="15a9b-101">Set-AzDiskUpdateDiskEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="15a9b-101">Set-AzDiskUpdateDiskEncryptionKey</span></span>

## <span data-ttu-id="15a9b-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="15a9b-102">SYNOPSIS</span></span>
<span data-ttu-id="15a9b-103">A lemezvezérlő-titkosítási kulcs tulajdonságait állítja be a Disk Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="15a9b-103">Sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="15a9b-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="15a9b-104">SYNTAX</span></span>

```
Set-AzDiskUpdateDiskEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-SecretUrl] <String>]
 [[-SourceVaultId] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="15a9b-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="15a9b-105">DESCRIPTION</span></span>
<span data-ttu-id="15a9b-106">A **set-AzDiskUpdateDiskEncryptionKey** parancsmag a Disk Encryption Key tulajdonságát a Disk Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="15a9b-106">The **Set-AzDiskUpdateDiskEncryptionKey** cmdlet sets the disk encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="15a9b-107">Példák</span><span class="sxs-lookup"><span data-stu-id="15a9b-107">EXAMPLES</span></span>

### <span data-ttu-id="15a9b-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="15a9b-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -SkuName Premium_LRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="15a9b-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="15a9b-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="15a9b-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="15a9b-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="15a9b-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="15a9b-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="15a9b-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="15a9b-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="15a9b-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="15a9b-113">PARAMETERS</span></span>

### <span data-ttu-id="15a9b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a9b-114">-DefaultProfile</span></span>
<span data-ttu-id="15a9b-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="15a9b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15a9b-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="15a9b-116">-DiskUpdate</span></span>
<span data-ttu-id="15a9b-117">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="15a9b-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15a9b-118">-SecretUrl</span><span class="sxs-lookup"><span data-stu-id="15a9b-118">-SecretUrl</span></span>
<span data-ttu-id="15a9b-119">A titkos URL-címet adja meg.</span><span class="sxs-lookup"><span data-stu-id="15a9b-119">Specifies the secret Url.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a9b-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="15a9b-120">-SourceVaultId</span></span>
<span data-ttu-id="15a9b-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="15a9b-121">Specifies the source vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15a9b-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="15a9b-122">-Confirm</span></span>
<span data-ttu-id="15a9b-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="15a9b-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a9b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15a9b-124">-WhatIf</span></span>
<span data-ttu-id="15a9b-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="15a9b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15a9b-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="15a9b-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15a9b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a9b-127">CommonParameters</span></span>
<span data-ttu-id="15a9b-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="15a9b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a9b-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="15a9b-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a9b-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a9b-130">INPUTS</span></span>

### <span data-ttu-id="15a9b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="15a9b-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="15a9b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="15a9b-132">System.String</span></span>

## <span data-ttu-id="15a9b-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="15a9b-133">OUTPUTS</span></span>

### <span data-ttu-id="15a9b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="15a9b-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="15a9b-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="15a9b-135">NOTES</span></span>

## <span data-ttu-id="15a9b-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="15a9b-136">RELATED LINKS</span></span>
