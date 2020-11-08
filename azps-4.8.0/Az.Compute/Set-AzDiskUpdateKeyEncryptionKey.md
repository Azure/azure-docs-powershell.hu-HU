---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskupdatekeyencryptionkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskUpdateKeyEncryptionKey.md
ms.openlocfilehash: d37181ae14b0070cd60adca3f6f56f25eab7fd3e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94181167"
---
# <span data-ttu-id="f6345-101">Set-AzDiskUpdateKeyEncryptionKey</span><span class="sxs-lookup"><span data-stu-id="f6345-101">Set-AzDiskUpdateKeyEncryptionKey</span></span>

## <span data-ttu-id="f6345-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="f6345-102">SYNOPSIS</span></span>
<span data-ttu-id="f6345-103">A kulcs titkosítási kulcs tulajdonságait állítja be a lemez Update objektumban.</span><span class="sxs-lookup"><span data-stu-id="f6345-103">Sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="f6345-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="f6345-104">SYNTAX</span></span>

```
Set-AzDiskUpdateKeyEncryptionKey [-DiskUpdate] <PSDiskUpdate> [[-KeyUrl] <String>] [[-SourceVaultId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6345-105">Leírás</span><span class="sxs-lookup"><span data-stu-id="f6345-105">DESCRIPTION</span></span>
<span data-ttu-id="f6345-106">A **set-AzDiskUpdateKeyEncryptionKey** parancsmag a kulcs titkosítási kulcs tulajdonságát a Disk Update objektumban állítja be.</span><span class="sxs-lookup"><span data-stu-id="f6345-106">The **Set-AzDiskUpdateKeyEncryptionKey** cmdlet sets the key encryption key properties on a disk update object.</span></span>

## <span data-ttu-id="f6345-107">Példák</span><span class="sxs-lookup"><span data-stu-id="f6345-107">EXAMPLES</span></span>

### <span data-ttu-id="f6345-108">Példa 1</span><span class="sxs-lookup"><span data-stu-id="f6345-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption Empty -EncryptionSettingsEnabled $true;
PS C:\> $secretUrl = https://myvault.vault-int.azure-int.net/secrets/123/;
PS C:\> $secretId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault123';
PS C:\> $keyUrl = https://myvault.vault-int.azure-int.net/keys/456;
PS C:\> $keyId = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.KeyVault/vaults/TestVault456';
PS C:\> $diskupdateconfig = Set-AzDiskUpdateDiskEncryptionKey -DiskUpdate $diskupdateconfig -SecretUrl $secretUrl -SourceVaultId $secretId;
PS C:\> $diskupdateconfig = Set-AzDiskUpdateKeyEncryptionKey -DiskUpdate $diskupdateconfig -KeyUrl $keyUrl -SourceVaultId $keyId;
PS C:\> Update-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="f6345-109">Az első parancs létrehoz egy helyi üres Disk Update-objektumot, a 10GB méretet Premium_LRS tárterület-fiók típusában.</span><span class="sxs-lookup"><span data-stu-id="f6345-109">The first command creates a local empty disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f6345-110">A beállítás a Windows operációs rendszer típusa és a titkosítási beállítások megadását is lehetővé teszi.</span><span class="sxs-lookup"><span data-stu-id="f6345-110">It also sets Windows OS type and enables encryption settings.</span></span>
<span data-ttu-id="f6345-111">A második és a harmadik parancs a Disk Update objektum merevlemez-titkosítási kulcsát és kulcs-titkosítási kulcsának beállítását adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6345-111">The second and third commands set the disk encryption key and key encryption key settings for the disk update object.</span></span>
<span data-ttu-id="f6345-112">Az utolsó parancs átveszi a Disk Update objektumot, és frissíti a meglévő, "Disk01" nevű lemezt az erőforráscsoport "ResourceGroup01" csoportjában.</span><span class="sxs-lookup"><span data-stu-id="f6345-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f6345-113">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="f6345-113">PARAMETERS</span></span>

### <span data-ttu-id="f6345-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6345-114">-DefaultProfile</span></span>
<span data-ttu-id="f6345-115">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="f6345-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6345-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f6345-116">-DiskUpdate</span></span>
<span data-ttu-id="f6345-117">Helyi merevlemez-frissítő objektum megadása</span><span class="sxs-lookup"><span data-stu-id="f6345-117">Specifies a local disk update object.</span></span>

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

### <span data-ttu-id="f6345-118">-KeyUrl</span><span class="sxs-lookup"><span data-stu-id="f6345-118">-KeyUrl</span></span>
<span data-ttu-id="f6345-119">A kulcs URL-címét adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6345-119">Specifies the key Url.</span></span>

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

### <span data-ttu-id="f6345-120">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="f6345-120">-SourceVaultId</span></span>
<span data-ttu-id="f6345-121">A forrás boltozat-AZONOSÍTÓját adja meg.</span><span class="sxs-lookup"><span data-stu-id="f6345-121">Specifies the source vault ID.</span></span>

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

### <span data-ttu-id="f6345-122">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="f6345-122">-Confirm</span></span>
<span data-ttu-id="f6345-123">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="f6345-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6345-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6345-124">-WhatIf</span></span>
<span data-ttu-id="f6345-125">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="f6345-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f6345-126">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="f6345-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6345-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6345-127">CommonParameters</span></span>
<span data-ttu-id="f6345-128">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="f6345-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6345-129">További információt a [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)című témakörben talál.</span><span class="sxs-lookup"><span data-stu-id="f6345-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6345-130">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6345-130">INPUTS</span></span>

### <span data-ttu-id="f6345-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f6345-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

### <span data-ttu-id="f6345-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f6345-132">System.String</span></span>

## <span data-ttu-id="f6345-133">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="f6345-133">OUTPUTS</span></span>

### <span data-ttu-id="f6345-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f6345-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate</span></span>

## <span data-ttu-id="f6345-135">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="f6345-135">NOTES</span></span>

## <span data-ttu-id="f6345-136">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="f6345-136">RELATED LINKS</span></span>
