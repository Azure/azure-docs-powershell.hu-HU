---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CC306D8C-A5EE-4655-B686-E5A77CCE5042
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmchefextension
schema: 2.0.0
ms.openlocfilehash: 277790badbaeef02139034ffd32f639f90929133
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: hu-HU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850433"
---
# <span data-ttu-id="2355f-101">Set-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2355f-101">Set-AzureRmVMChefExtension</span></span>

## <span data-ttu-id="2355f-102">Áttekintés</span><span class="sxs-lookup"><span data-stu-id="2355f-102">SYNOPSIS</span></span>
<span data-ttu-id="2355f-103">Kibővíti a séf kiterjesztését egy virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2355f-103">Adds a Chef extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2355f-104">SZINTAXISA</span><span class="sxs-lookup"><span data-stu-id="2355f-104">SYNTAX</span></span>

### <span data-ttu-id="2355f-105">Linux</span><span class="sxs-lookup"><span data-stu-id="2355f-105">Linux</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Linux] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2355f-106">Windows</span><span class="sxs-lookup"><span data-stu-id="2355f-106">Windows</span></span>
```
Set-AzureRmVMChefExtension [-ResourceGroupName] <String> [-VMName] <String> [[-TypeHandlerVersion] <String>]
 -ValidationPem <String> [-ClientRb <String>] [-BootstrapOptions <String>] [-JsonAttribute <String>]
 [-ChefDaemonInterval <String>] [-Daemon <String>] [-Secret <String>] [-SecretFile <String>]
 [-RunList <String>] [-ChefServerUrl <String>] [-ValidationClientName <String>] [-OrganizationName <String>]
 [-BootstrapVersion <String>] [-Windows] [[-Location] <String>] [[-Name] <String>]
 [[-AutoUpgradeMinorVersion] <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2355f-107">Leírás</span><span class="sxs-lookup"><span data-stu-id="2355f-107">DESCRIPTION</span></span>
<span data-ttu-id="2355f-108">A **set-AzureVMChefExtension** parancsmag hozzáadja a Chef bővítményt a virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2355f-108">The **Set-AzureVMChefExtension** cmdlet adds the Chef extension to the virtual machine.</span></span>

## <span data-ttu-id="2355f-109">Példák</span><span class="sxs-lookup"><span data-stu-id="2355f-109">EXAMPLES</span></span>

### <span data-ttu-id="2355f-110">1. példa: Chef-kiterjesztés hozzáadása Windows Virtual Machine-géphez</span><span class="sxs-lookup"><span data-stu-id="2355f-110">Example 1: Add a Chef extension to a Windows virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup001" -VMName "WindowsVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Daemon "service" -SecretFile "C:\my_encrypted_data_bag_secret" -Windows
```

<span data-ttu-id="2355f-111">Ez a parancs egy WindowsVM001 nevű Windows Virtual Machine-bővítményt ad hozzá a Szakácshoz.</span><span class="sxs-lookup"><span data-stu-id="2355f-111">This command adds a Chef extension to a Windows virtual machine named WindowsVM001.</span></span>
<span data-ttu-id="2355f-112">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="2355f-112">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2355f-113">2. példa: Chef-kiterjesztés hozzáadása egy linuxos virtuális géphez</span><span class="sxs-lookup"><span data-stu-id="2355f-113">Example 2: Add a Chef extension to a Linux virtual machine</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup002" -VMName "LinuxVM001" -ValidationPem "C:\my-org-validator.pem" -ClientRb "C:\client.rb" -RunList "Apache" -Secret "my_secret" -Linux
```

<span data-ttu-id="2355f-114">Ez a parancs hozzáadja a Chef bővítményt egy LinuxVM001 nevű linuxos virtuális géphez.</span><span class="sxs-lookup"><span data-stu-id="2355f-114">This command adds a Chef extension to a Linux virtual machine named LinuxVM001.</span></span>
<span data-ttu-id="2355f-115">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="2355f-115">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>

### <span data-ttu-id="2355f-116">3. példa: a Chef Extension bővítmény felvétele Windows Virtual Machine-be bootstrap beállításokkal</span><span class="sxs-lookup"><span data-stu-id="2355f-116">Example 3: Add a Chef extension to a Windows virtual machine with bootstrap options</span></span>
```
PS C:\> Set-AzureRmVMChefExtension -ResourceGroupName "ResourceGroup003" -VMName "WindowsVM002" -ValidationPem C:\my-org-validator.pem -ClientRb C:\client.rb -BootstrapOptions '{"chef_node_name":"your_node_name","chef_server_url":"https://api.opscode.com/organizations/some-org", "validation_client_name":"some-org-validator"}' -RunList "Apache" -Windows
```

<span data-ttu-id="2355f-117">Ez a parancs hozzáadja a Chef kiterjesztését egy WindowsVM002 nevű Windows Virtual Machine-géphez.</span><span class="sxs-lookup"><span data-stu-id="2355f-117">This command adds the Chef extension to a Windows virtual machine named WindowsVM002.</span></span>
<span data-ttu-id="2355f-118">Amikor elindul a virtuális gép, a séf a virtuális gépet az Apache-hoz futtatja.</span><span class="sxs-lookup"><span data-stu-id="2355f-118">When the virtual machine starts, Chef bootstraps the virtual machine to run Apache.</span></span>
<span data-ttu-id="2355f-119">A rendszerindítás után a virtuális gép a JSON formátumban megadott BootstrapOptions hivatkozik.</span><span class="sxs-lookup"><span data-stu-id="2355f-119">After bootstrapping, the virtual machine refers to the BootstrapOptions specified in JSON format.</span></span>

## <span data-ttu-id="2355f-120">PARAMÉTEREK</span><span class="sxs-lookup"><span data-stu-id="2355f-120">PARAMETERS</span></span>

### <span data-ttu-id="2355f-121">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="2355f-121">-AutoUpgradeMinorVersion</span></span>
```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-122">-BootstrapOptions</span><span class="sxs-lookup"><span data-stu-id="2355f-122">-BootstrapOptions</span></span>
<span data-ttu-id="2355f-123">A client_rb beállítás beállítási beállításait adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-123">Specifies configuration settings in the client_rb option.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-124">-BootstrapVersion</span><span class="sxs-lookup"><span data-stu-id="2355f-124">-BootstrapVersion</span></span>
<span data-ttu-id="2355f-125">A bootstrap-konfiguráció verziószámát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-125">Specifies the version of the bootstrap configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-126">-ChefDaemonInterval</span><span class="sxs-lookup"><span data-stu-id="2355f-126">-ChefDaemonInterval</span></span>
<span data-ttu-id="2355f-127">Annak gyakoriságát adja meg (percben), amikor a séf-szolgáltatás fut.</span><span class="sxs-lookup"><span data-stu-id="2355f-127">Specifies the frequency (in minutes) at which the chef-service runs.</span></span> <span data-ttu-id="2355f-128">Ha abban az esetben, ha nem szeretné, hogy a séf-szolgáltatás telepítve legyen az Azure VM-ben, akkor ebben a mezőben a 0 értéket adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-128">If in case you don't want the chef-service to be installed on the Azure VM then set value as 0 in this field.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ChefServiceInterval

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-129">-ChefServerUrl</span><span class="sxs-lookup"><span data-stu-id="2355f-129">-ChefServerUrl</span></span>
<span data-ttu-id="2355f-130">A séf-kiszolgáló hivatkozását adja meg URL-címként.</span><span class="sxs-lookup"><span data-stu-id="2355f-130">Specifies the Chef server link, as a URL.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-131">-ClientRb</span><span class="sxs-lookup"><span data-stu-id="2355f-131">-ClientRb</span></span>
<span data-ttu-id="2355f-132">A Chef Client. RB teljes elérési útját adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-132">Specifies the full path of the Chef client.rb.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-133">-Daemon</span><span class="sxs-lookup"><span data-stu-id="2355f-133">-Daemon</span></span>
<span data-ttu-id="2355f-134">A Chef-Client szolgáltatás beállítása felügyelet nélküli végrehajtáshoz.</span><span class="sxs-lookup"><span data-stu-id="2355f-134">Configures the chef-client service for unattended execution.</span></span> <span data-ttu-id="2355f-135">A csomópont platformjának Windows rendszernek kell lennie.</span><span class="sxs-lookup"><span data-stu-id="2355f-135">The node platform should be Windows.</span></span>
<span data-ttu-id="2355f-136">Engedélyezett beállítások: "nincs", "szolgáltatás" és "tevékenység".</span><span class="sxs-lookup"><span data-stu-id="2355f-136">Allowed options: 'none','service' and 'task'.</span></span>
<span data-ttu-id="2355f-137">nincs – ez a beállítás megakadályozza a Chef-Client szolgáltatás szolgáltatásként való konfigurálását.</span><span class="sxs-lookup"><span data-stu-id="2355f-137">none - Currently prevents the chef-client service from being configured as a service.</span></span>
<span data-ttu-id="2355f-138">szolgáltatás – beállítja a séf – ügyfelet, hogy szolgáltatásként automatikusan fusson a háttérben.</span><span class="sxs-lookup"><span data-stu-id="2355f-138">service - Configures the chef-client to run automatically in the background as a service.</span></span>
<span data-ttu-id="2355f-139">feladat – úgy állítja be a Chef-clientt, hogy automatikusan fusson a háttérben secheduled tevékenységként.</span><span class="sxs-lookup"><span data-stu-id="2355f-139">task - Configures the chef-client to run automatically in the background as a secheduled task.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: none, service, task

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2355f-140">-DefaultProfile</span></span>
<span data-ttu-id="2355f-141">Az azuretal való kommunikációhoz használt hitelesítő adatok, fiók, bérlői fiók és előfizetés.</span><span class="sxs-lookup"><span data-stu-id="2355f-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2355f-142">-JsonAttribute</span><span class="sxs-lookup"><span data-stu-id="2355f-142">-JsonAttribute</span></span>
<span data-ttu-id="2355f-143">A Chef-Client első futtatásához hozzáadni kívánt JSON-karakterlánc.</span><span class="sxs-lookup"><span data-stu-id="2355f-143">A JSON string to be added to the first run of chef-client.</span></span> <span data-ttu-id="2355f-144">például-JsonAttribute ' {"foo": "sáv"} '</span><span class="sxs-lookup"><span data-stu-id="2355f-144">e.g. -JsonAttribute '{"foo" : "bar"}'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-145">-Linux</span><span class="sxs-lookup"><span data-stu-id="2355f-145">-Linux</span></span>
<span data-ttu-id="2355f-146">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="2355f-146">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-147">-Hely</span><span class="sxs-lookup"><span data-stu-id="2355f-147">-Location</span></span>
<span data-ttu-id="2355f-148">A virtuális gép helyét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-148">Specifies the location of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-149">-Name (név)</span><span class="sxs-lookup"><span data-stu-id="2355f-149">-Name</span></span>
<span data-ttu-id="2355f-150">A Szakácsi mellék nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-150">Specifies the name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-151">-Szervezetnév</span><span class="sxs-lookup"><span data-stu-id="2355f-151">-OrganizationName</span></span>
<span data-ttu-id="2355f-152">A séf-kiterjesztés szervezeti nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-152">Specifies the organization name of the Chef extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2355f-153">-ResourceGroupName</span></span>
<span data-ttu-id="2355f-154">A virtuális gépet tartalmazó erőforráscsoport nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-154">Specifies the name of the resource group that contains the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-155">-RunList</span><span class="sxs-lookup"><span data-stu-id="2355f-155">-RunList</span></span>
<span data-ttu-id="2355f-156">A Chef Node Run (sorozat) lista.</span><span class="sxs-lookup"><span data-stu-id="2355f-156">Specifies the Chef node run list.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-157">-Secret</span><span class="sxs-lookup"><span data-stu-id="2355f-157">-Secret</span></span>
<span data-ttu-id="2355f-158">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcs.</span><span class="sxs-lookup"><span data-stu-id="2355f-158">The encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-159">-SecretFile</span><span class="sxs-lookup"><span data-stu-id="2355f-159">-SecretFile</span></span>
<span data-ttu-id="2355f-160">Az adattáska-elem értékeinek titkosításához és visszafejtéséhez használt titkosítási kulcsot tartalmazó fájl elérési útja.</span><span class="sxs-lookup"><span data-stu-id="2355f-160">The path to the file that contains the encryption key used to encrypt and decrypt the data bag item values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-161">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="2355f-161">-TypeHandlerVersion</span></span>
<span data-ttu-id="2355f-162">Annak a bővítménynek a verziószámát adja meg, amelyet a virtuális géphez használni szeretne.</span><span class="sxs-lookup"><span data-stu-id="2355f-162">Specifies the version of the extension to use for this virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-163">-ValidationClientName</span><span class="sxs-lookup"><span data-stu-id="2355f-163">-ValidationClientName</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-164">-ValidationPem</span><span class="sxs-lookup"><span data-stu-id="2355f-164">-ValidationPem</span></span>
<span data-ttu-id="2355f-165">A Chef validator. PEM fájl elérési útvonalát adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-165">Specifies the Chef validator .pem file path</span></span>

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

### <span data-ttu-id="2355f-166">-VMName</span><span class="sxs-lookup"><span data-stu-id="2355f-166">-VMName</span></span>
<span data-ttu-id="2355f-167">A virtuális gép nevét adja meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-167">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="2355f-168">Ez a parancsmag hozzáadja a Chef bővítményt a virtuális géphez, amelyet ez a paraméter határoz meg.</span><span class="sxs-lookup"><span data-stu-id="2355f-168">This cmdlet adds the Chef extension for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-169">-Windows</span><span class="sxs-lookup"><span data-stu-id="2355f-169">-Windows</span></span>
<span data-ttu-id="2355f-170">Jelzi, hogy ez a parancsmag létrehoz egy Windows Virtual Machine-t.</span><span class="sxs-lookup"><span data-stu-id="2355f-170">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-171">– Megerősítés</span><span class="sxs-lookup"><span data-stu-id="2355f-171">-Confirm</span></span>
<span data-ttu-id="2355f-172">A parancsmag futtatása előtt kéri a megerősítést.</span><span class="sxs-lookup"><span data-stu-id="2355f-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2355f-173">-WhatIf</span></span>
<span data-ttu-id="2355f-174">Annak megjelenítése, hogy mi történik, ha a parancsmag fut.</span><span class="sxs-lookup"><span data-stu-id="2355f-174">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="2355f-175">A parancsmag nem fut.</span><span class="sxs-lookup"><span data-stu-id="2355f-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2355f-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2355f-176">CommonParameters</span></span>
<span data-ttu-id="2355f-177">Ez a parancsmag a következő általános paramétereket támogatja:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-,-PipelineVariable-WarningAction</span><span class="sxs-lookup"><span data-stu-id="2355f-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2355f-178">További információ: about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2355f-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2355f-179">BEMENETEK</span><span class="sxs-lookup"><span data-stu-id="2355f-179">INPUTS</span></span>

### <span data-ttu-id="2355f-180">Nincs</span><span class="sxs-lookup"><span data-stu-id="2355f-180">None</span></span>
<span data-ttu-id="2355f-181">Ez a parancsmag nem fogadja el a bevitelt.</span><span class="sxs-lookup"><span data-stu-id="2355f-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="2355f-182">KIMENETEK</span><span class="sxs-lookup"><span data-stu-id="2355f-182">OUTPUTS</span></span>

### <span data-ttu-id="2355f-183">Microsoft. Azure. commands. kiszámítás. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2355f-183">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2355f-184">MEGJEGYZI</span><span class="sxs-lookup"><span data-stu-id="2355f-184">NOTES</span></span>

## <span data-ttu-id="2355f-185">KAPCSOLÓDÓ HIVATKOZÁSOK</span><span class="sxs-lookup"><span data-stu-id="2355f-185">RELATED LINKS</span></span>

[<span data-ttu-id="2355f-186">Get-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2355f-186">Get-AzureRmVMChefExtension</span></span>](./Get-AzureRmVMChefExtension.md)

[<span data-ttu-id="2355f-187">Remove-AzureRmVMChefExtension</span><span class="sxs-lookup"><span data-stu-id="2355f-187">Remove-AzureRmVMChefExtension</span></span>](./Remove-AzureRmVMChefExtension.md)
